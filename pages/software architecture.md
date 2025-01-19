- examens questions
	- Fault Tolerance desiderata: What are they, and how does the Akka Actor system address them?
		- The fault tolerance infrastructure desiderata are a set of requirements that a system should meet to be able to handle faults effectively. The Akka Actor system provides solutions to these requirements.
		- **Support Component Compartmentalization**: A faulty component should be isolated from others to prevent the fault from escalating to a total system crash.
			- Akka actors are supervised and organized hierarchically. A supervisor can decide to terminate a faulty actor, removing it from the system, and the hierarchy enables replacing actors at runtime.
		- **Support Suspension of Component Interactions**: Calls to a faulty component should be suspended until the component is fixed or replaced, enabling a smooth continuation of work.
			- If an Akka actor crashes, its mailbox is suspended until its supervisor decides how to handle the failure.
		- **Provide Component Lifecycle Management**: Isolate faulty components and terminate and remove or re-initialize components that cannot recover.
			- Akka actors are active components that can be started, stopped, and restarted, providing lifecycle management capabilities.
		- **Enable Separation of Concerns**: Fault recovery code, which is a cross-cutting concern, should be separated from normal processing code.
		- In Akka, actor message processing logic is separated from fault recovery logic, allowing them to be defined and evolve independently.
		  
		  Akka implements the **Let-it-crash** pattern through parental supervision, where supervisors handle failures of their child actors and decide on appropriate recovery actions. The available fault recovery options for supervisors include restarting the actor, resuming the actor, stopping the actor, or escalating the failure to a higher-level supervisor.
		  
		  The example of a log processing application illustrates how Akka supports fault tolerance. In this application, the `LogProcessingGuardian` actor supervises `FileWatcher` actors that monitor log files in specific directories. Each `FileWatcher` actor spawns a `LogProcessor` actor to parse the log files and a `DbWriter` actor to write the parsed data to a database. The system is designed with risky operations delegated to lower-level actors, allowing higher-level supervisors to handle potential failures effectively. For instance, if the `DbWriter` actor encounters a database connection error, its supervisor (`LogProcessor`) can attempt to create a new `DbWriter` actor using an alternative database URL. This hierarchical supervision structure helps contain failures and prevent them from cascading throughout the system.
-