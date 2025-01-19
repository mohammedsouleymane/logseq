- examens questions
	- Fault Tolerance desiderata: What are they, and how does the Akka Actor system address them?
	  collapsed:: true
		- The fault tolerance infrastructure desiderata are a set of requirements that a system should meet to be able to handle faults effectively. The Akka Actor system provides solutions to these requirements.
		- **Support Component Compartmentalization**: A faulty component should be isolated from others to prevent the fault from escalating to a total system crash.
			- Akka actors are supervised and organized hierarchically. A supervisor can decide to terminate a faulty actor, removing it from the system, and the hierarchy enables replacing actors at runtime.
		- **Support Suspension of Component Interactions**: Calls to a faulty component should be suspended until the component is fixed or replaced, enabling a smooth continuation of work.
			- If an Akka actor crashes, its mailbox is suspended until its supervisor decides how to handle the failure.
		- **Provide Component Lifecycle Management**: Isolate faulty components and terminate and remove or re-initialize components that cannot recover.
			- Akka actors are active components that can be started, stopped, and restarted, providing lifecycle management capabilities.
		- **Enable Separation of Concerns**: Fault recovery code, which is a cross-cutting concern, should be separated from normal processing code.
			- In Akka, actor message processing logic is separated from fault recovery logic, allowing them to be defined and evolve independently.
	- Write code for a Counter actor that counts received messages and can return the count. Implement it with and without field assignment.
	  collapsed:: true
		- ### Counter Actor with Field Assignment
		  
		  This implementation uses a field to store the current count.
		  
		  ```
		  object CounterWithField {
		  sealed trait Command
		  case object Increment extends Command
		  case object GetCount extends Command
		  final case class Count(value: Int)
		  
		  def apply(): Behavior[Command] = Behaviors.setup { context =>
		    var count = 0
		  
		    Behaviors.receiveMessage { message =>
		      message match {
		        case Increment =>
		          count += 1
		          Behaviors.same
		        case GetCount =>
		          context.replyTo ! Count(count)
		          Behaviors.same
		      }
		    }
		  }
		  }
		  ```
		  
		  This code defines:
		- A sealed trait `Command` representing the messages the actor can receive.
		- A case object `Increment` for incrementing the counter.
		- A case object `GetCount` for requesting the current count.
		- A case class `Count` to hold the count value when replying to `GetCount`.
		- The `apply` method returns the initial behavior of the actor.
			- It initializes a mutable variable `count` to 0.
			- The `Behaviors.receiveMessage` block defines how the actor handles incoming messages.
				- For `Increment`, it increments the `count` and returns `Behaviors.same`, indicating that the actor's behavior remains unchanged.
				- For `GetCount`, it sends the current `count` wrapped in a `Count` message to the `context.replyTo` (the sender of the `GetCount` message) and returns `Behaviors.same`.
				  
				  This implementation demonstrates the basic structure of an Akka actor and how it can be used to maintain and update state.
		- ### Counter Actor without Field Assignment
		  
		  This implementation uses a recursive function to pass the current count between invocations of the behavior function, avoiding field assignment.
		  
		  ```
		  object CounterWithoutField {
		  sealed trait Command
		  case object Increment extends Command
		  case object GetCount extends Command
		  final case class Count(value: Int)
		  
		  def apply(count: Int = 0): Behavior[Command] = Behaviors.receiveMessage {
		    message =>
		      message match {
		        case Increment =>
		          apply(count + 1)
		        case GetCount =>
		          context.replyTo ! Count(count)
		          Behaviors.same
		      }
		  }
		  }
		  ```
		  
		  This code is similar to the previous example but with these key differences:
		- The `apply` method takes an optional `count` parameter, defaulting to 0, and returns a `Behavior[Command]`.
		- It directly uses `Behaviors.receiveMessage` to handle messages.
			- For `Increment`, it calls `apply` again with the incremented count, effectively creating a new behavior with the updated count.
			- For `GetCount`, it behaves the same as the previous example.
			  
			  This implementation showcases a more functional approach to state management in Akka actors by using recursion and immutability.
			  
			  **Both implementations achieve the same goal of counting received messages and providing the count.** Choosing between them depends on your preference for a more object-oriented (with field assignment) or functional (without field assignment) style. The second implementation is **generally considered more idiomatic in the Akka world** due to its emphasis on immutability and functional programming principles.
			  
			  <!--EndFragment-->
	- Architectural problems solved by the Layer pattern.
	  collapsed:: true
		- The Layer pattern is a module pattern that addresses the need to develop and evolve portions of complex software systems independently [1, 2]. This pattern divides software into units called layers, with each layer being a grouping of modules that offers a cohesive set of services [2]. Each layer has a public interface, and usage between layers must be **unidirectional**. For example, layer *n* can use the services of layer *n-1* but cannot use the services of layer *n+1* [3, 4].
		  
		  The Layer pattern has several strengths:
		- It promotes **modifiability, reuse, and portability** because layers can be developed and evolved separately [4].
		- It achieves **separation of concerns** by grouping related modules into layers [4].
		- It **manages complexity** and facilitates communication by providing a clear structure of the codebase [4].
		  
		  However, it also has a weakness. Adding layers adds **up-front cost and complexity** to a system [4].
		  
		  The Dependency Inversion pattern (also known as the Onion pattern) offers an alternative approach to layering [5]. In the traditional, procedural interpretation of the Layer pattern, high-level layers (e.g., business logic) depend on low-level, utilitarian layers (e.g., persistence). This creates a downward dependency direction [6].
		  
		  **Dependency inversion flips this relationship.** The high-level layer declares interfaces, and the low-level layer implements those interfaces. This creates an inward coupling direction, with outer, low-level layers depending on inner, high-level layers [6].
		  
		  Here's a comparison of where the high-level layers are located in each pattern:
		- **Layer pattern**: High-level layers are at the **top**, depending on the lower-level layers beneath them.
		- **Dependency Inversion (Onion) pattern**: High-level layers are at the **core**, with the lower-level layers depending on them.
		  
		  Dependency Inversion offers several advantages:
		- **Changes to the lower-level layers do not affect the inner, high-level layers.** This means the inner layers can be compiled, run, and tested independently, potentially improving development speed and reducing the need to run time-consuming integration tests [6].
		- **Flexibility is increased**. For example, it's easier to swap out an outer layer for a mock implementation when testing an inner layer [7].
		  
		  The "Cake pattern," which uses Scala language constructs like self types, is one way to implement dependency inversion [8]. However, it can be complex to understand and implement correctly [9]. Another approach is to use dependency injection frameworks, which automatically create and inject instances of dependencies [8]. These frameworks can simplify development but introduce an external dependency on the framework itself [10].
	- Role of the ephemeral child in the aggregator pattern. Include a diagram
	  collapsed:: true
		- The Aggregator pattern is used to collect responses from multiple services and combine them into a single result. [1] The **ephemeral child** plays a vital role in this pattern by simplifying the process of aggregating results from multiple asynchronous operations. It acts as a temporary actor dedicated to receiving and processing responses from the various services involved in fulfilling the request.
		- Here's a breakdown of the role of the ephemeral child, illustrated with a diagram
		- ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGQMvIVX9piqi5sV3V0aL1j92zdt1JUNUUmE1N_OpixLwZXLClW8OZTxbkK6yJX0FyYV6QEzykT8dhta-C5Ami9BaWJLjqSI9N6EQ_s1N8SRr__emBqOMSIvyY1aQEYhEhqKH03Q?key=2EMOWLWo9n_tfDzOLam1Il8W)
		-
		- **Benefits of Using an Ephemeral Child:**
			- **Simplified State Management:** The aggregator child encapsulates the logic for collecting and combining results, reducing complexity in the parent actor.
			- **Improved Responsiveness:** Parallel requests to services enhance overall response time.
			- **Clean Code Structure:** The ephemeral nature of the child ensures automatic cleanup after task completion, leading to more readable and maintainable code.
	- Sketch and explain the Ask pattern and its variant using an ephemeral child.
	  collapsed:: true
		- The **Ask pattern** is a messaging pattern used in actor-based systems to **reliably request a response from an actor**. It addresses the challenge of handling responses to requests in asynchronous messaging environments where the requester and responder actors operate concurrently.
		  
		  **Challenges Addressed by the Ask Pattern:**
		- **Correlating Responses with Requests**: In asynchronous messaging, responses might arrive out of order or with delays. The Ask pattern helps match responses to the original requests.
		- **Handling Timeouts**: The Ask pattern provides mechanisms to handle situations where a response is not received within a specified timeframe.
		- **Avoiding Protocol Pollution**: Directly handling responses within the requester actor can clutter its protocol and make it susceptible to errors caused by mismatched responses.
		  
		  **Core Idea of the Ask Pattern:**
		  
		  The essence of the Ask pattern is to **delegate the handling of a response to a dedicated, short-lived component**. This dedicated component, typically an ephemeral child actor, is spawned by the requester actor for each request. The child actor acts as a proxy, receiving the response from the responder actor and forwarding it to the original requester. This approach ensures that:
		- Responses are correctly correlated with their corresponding requests.
		- Timeouts can be managed by the child actor, keeping the requester's logic clean.
		- The requester actor's message protocol remains uncluttered by response handling.
		  
		  **Implementation of the Ask Pattern Using an Ephemeral Child:**
		- **Requester Sends Request with Reply-To**: The requester actor sends the request message to the responder actor, including the address of the ephemeral child actor as the "reply-to" address.
		- **Ephemeral Child Handles Response**: The responder actor sends the response to the ephemeral child actor.
		- **Child Forwards Response to Requester**: The child actor receives the response and forwards it to the original requester actor.
		- **Child Terminates**: Once the response is forwarded, the ephemeral child actor terminates, ensuring it doesn't interfere with future requests.
		  
		  **Benefits of Using an Ephemeral Child:**
		- **Isolation**: The child actor isolates the response handling logic from the requester actor.
		- **Cleanup**: The child actor automatically terminates after fulfilling its purpose, simplifying resource management.
		- **Error Handling**: The child actor can handle timeouts and errors specific to the request, providing a localized error handling mechanism.
		  
		  The Ask pattern with an ephemeral child is a common and powerful technique in Akka actor systems. It promotes clean code, improves reliability, and simplifies the management of asynchronous communication between actors.
		- ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf2fH61ORywAcpwDGla-12fhEkHd5hoqI7dptd1_3lr7t75mSN_g9RqFoS9crtIK628h7PBHMavlCFAL6yORUILPKSAbt0zm7z7C0SwxByh25fvEnuT-qQkir5OG4M8H3yHqHED7w?key=2EMOWLWo9n_tfDzOLam1Il8W)
	- Advantages of Service-Oriented Architecture (SOA) and the components/connectors contributing to them. (ILD)
	  collapsed:: true
		- Service-Oriented Architecture (SOA) offers several advantages for building distributed systems:
			- **Interoperability:** SOA promotes interoperability by enabling communication between components running on different platforms, potentially using different programming languages, and possibly residing across the internet. This is achieved through the use of standardized protocols and connectors like:
				- **SOAP connector**: Enables synchronous communication between web services, typically over HTTP, and uses WSDL (Web Service Description Language) for service descriptions.
				- **REST connector**: request/reply operations of HTTP for communication.
			- **Legacy System Integration:** SOA facilitates the integration of legacy systems by exposing their functionality as services. This allows modern applications to interact with older systems without requiring significant modifications to the legacy codebase.
			- **Dynamic Reconfiguration:** The loose coupling inherent in SOA, where service consumers and providers interact through well-defined interfaces, enables dynamic reconfiguration. This allows for adding, removing, or updating services at runtime without impacting other parts of the system. For example, a service registry can be used to discover available services at runtime, making the system more flexible and adaptable to change.
		- The following components and connectors contribute to realizing these advantages:
		- **Components:**
		- **Service Providers:** These components offer one or more services through published interfaces.
		- **Service Consumers:** These components use the services provided by service providers, either directly or through intermediaries.
		- **Service Registry:** A centralized repository where service providers register their services and service consumers discover available services. This fosters location transparency by decoupling service consumers from the physical location of service providers.
		- **Orchestration Server:** Coordinates interactions between service consumers and providers based on predefined business processes and workflows. Orchestration can be implemented using scripting languages or specialized workflow engines, providing a centralized point of control for complex interactions.
		  
		  **Connectors:**
		- **SOAP/REST connectors**, as described above, enable synchronous communication between services.
		- **Asynchronous messaging connector:** Uses a messaging system like a message queue to facilitate point-to-point or publish-subscribe asynchronous message exchanges. This decoupling allows independence, enhances scalability and resilience. 
		  
		  While SOA offers significant benefits, it's important to be aware of potential drawbacks, including the complexity of building and managing SOA systems, performance overhead introduced by the middleware layer, and the challenges of controlling the evolution of independently developed services.
	- Implement at-least-once and exactly-once delivery on top of at-most-once systems. Highlight where extra state needs to be maintained.
		- At-most-once delivery:
		- No state needs to be maintained by the sender or receiver, as the message is simply sent without
		  considering its successful arrival.
		- A message is thus delivered [0, 1] times.
		  At-least-once delivery:
		- State must be maintained by the sender so that it will keep resending the message until it receives
		  an acknowledgment from the recipient that the message has arrived, ensuring that the message has
		  been successfully delivered at least once.
		  • A message is thus delivered [1, ] times, as the acknowledgment message itself can also be lost.
		  Exactly-once delivery:
		  • The same principle as at-least-once delivery must be followed, but additional state must be maintained
		  by the receiver to ensure that the receiver processes the messages only once, even if the message arrives
		  multiple times due to a lost acknowledgment message.
		  • Messages can thus be delivered multiple times but will only be processed once.
-