- Causal Federated Learning
	- Why AI lags in Medicine
		- Data issue: data imbalance, lack of overall data, biased data set
		- Privacy and Legal Constraints: Regulations like GDPR and the complexity of data consent make sharing raw, private patient data between institutions extremely difficult
		- Institutional "Agendas": Different types of hospitals (government, private, non-profit) have varying legal definitions and incentives, further complicating data centralization.
	- Solution: Federated Learning
	  Federated Learning is presented as a privacy-preserving alternative to traditional centralized training. Instead of moving data to a central server, the model is move to the data.
		- Mechanism: Local institutions (hospitals, research centers) train local models on their own private data. They then send only model updates or weights to a central Federated Server. The server aggregates these updates to create a Global Model, which then redistributed back to the participants.
		- Key Advantages: It allow for collaboration and massive data scaling without ever exchanging raw, sensitive patient information. We are not exchanging data, your Honor.
		-
	- Open challenges of FL
	  While FL solves privacy issues, it introduces new technical and security hurdles:
		- Model Security: The system is vulnerable to poising attacks (where an adversary corrupts local data or models), man-in-the-middle attacks, and DDoS attack.
		- Overhead: There is significant computation overhead (running local training loops) and communication overhead (frequently uploading and downloading model updates).
		- Heterogeneity and Fairness: "Client drift" occurs when data across different different hospitals is too diverse. Furthermore, smaller institutions with less data may feel excluded if incentive mechanisms and fairness are not properly managed.
	- The intersection of FL and Causality
	  The document argues that the "Achilles heel" of current machine learning it its reliance on correlation rather than causation.
		- The ladder of Causation: Drawing on Judea Pearl's work, the author notes that standard AI only operates on the first rung (Association/Seeing).
		- Goal: To reach higher rungs like Intervention (Doing) and Counterfactuals (Imagining), researchers are developing Federated Causal Discovery.
		- Application: This approach is being used by the AIMS group at VUB to study cognitive deterioration in Multiple Sclerosis (MS) across and international network, allowing for explainable-by-design models that support causal interventions