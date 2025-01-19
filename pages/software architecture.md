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
-