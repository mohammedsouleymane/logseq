- Causal Federated Learning
	- Why AI lags in Medicine
		- Data issue: data imbalance, lack of overall data, biased data set
		- Privacy and Legal Constraints: Regulations like GDPR and the complexity of data consent make sharing raw, private patient data between institutions extremely difficult
		- Institutional "Agendas": Different types of hospitals (government, private, non-profit) have varying legal definitions and incentives, further complicating data centralization.
	- Solution: Federated Learning
	  Federated Learning is presented as a privacy-preserving alternative to traditional centralized training. Instead of moving data to a central server, the model is move to the data.
		- Mechanism: Local institutions (hospitals, research centers) train local models on their own private data. They then send only model updates or weights to a central Federated Server. The server aggregates these updates to create a Global Model, which then redistributed back to the participants.
		- Key Advantages: It allow for
		-