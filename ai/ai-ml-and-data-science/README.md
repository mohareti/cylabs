# AI/ML and Data Science

* What is the Difference between AI,ML and Deep Learning
  * Applied data science
  * Applied mathmatics
  * Computational Mathematical modeling
  * AI (data science, ML, Predictive Analytics, prescriptive analytics, Probability and Statistics)
  * Big Data
  * Cloud and MLOps
  * Quantum computing and Quantum machine learning
* Types:
  * Supervised learning
    * Bayesian classifiers
    * Decision Trees
    * Labelled data
      * Classification
        * Decision Tree Classification
        * Random Forest Classification
        * K-nearest Neighbor
          * Example : Spam or ham
      * Regression
        * Logistic Regression
        * Polynomial Regression
        * Support Vector Machines
          * Example : Give port numbers which are under attack and ML algo will tell if it DDOS/bot network
  * Unsupervised learning (Group similar data)
    * Clustering
      * K-means Clustering
      * Hierarchical Clustering
      * Principal Component Analysis
        * To reduce the dimensions
  * Association (finds the important relationship)
    * Apriori
    * Eclat
  * Reinforcement learning
  * Deep Learning
    * Artificial Neural network
    * Neural Network
* Convolutional neural networks (CNNs)
* Recursive neural networks (RNNs)
* Long short-term memory (LSTM)
* Shallow neural networks
* Autoencoders (AEs)
* Restricted Boltzmann machines
* Use cases:
  * Attack surface detection based on mathematical modeling
  * pre-ransomware activity detection
  * IOT
  * DDOS
  * DNS
  * Malware
  * Phishing emails
* Key Concepts
  * feature engineering
  * feature selection
  * feature selection methods: filter methods, wrapper methods, and embedded method
  * reduce the complexity
  * overfitting of the model
* One-hot encoding
* L1 and L2 loss
* accuracy
* We need continuous monitoring/information from following to investigate anomalies, suspicious activity, TTP's, IOC's, IOA's
* \- Asset Discovery
* \- Vulnerability Management
* \- Endpoint Security
* \- IDS
* \- IPS
* \- Firewall
* \- WAF
* \- Load Balancer
* \- DNS logs
* \- Sysmon logs
* \- SIEM
* \- Business application logs
* \- OS event logs
* \- Sign in Activity
* \- Email flow (Phishing emails)
* \- Threat specific to industry
* \- Honeypot
* \- Honey accounts
* \- current incident response strategy
* \- clients, applications, web and database servers, NIDSs, HIDs, firewalls
* Cyber Security Analytics Goals
*  \- reduces the time for remediation
*  \- automated threat discovery/detection
*  \- discovering new suspicious patterns
* define few use cases to implement Cyber Security Analytics
* \- Malicious activity detection with out using known IOC's
* \- Behavioral Analytics
* \- Network traffic patterns
* \- phishing Email detection (email header analysis, url links)
* \- Botnet analysis
* \- Learning historical SIEM/network data
* Data
* structured
* semi structured
* un structured
* labeled and unlabeled data
* what is our problem ?
* what we are expecting to solve ?
* what is training and Testing data ratio ?
* From where we are getting this ?
* Model overfitting issue
* Model underfitting issue
* negative biases
* Types ML
* \- supervised
* phishing email detection
* \- Deep Learning
* \- Un-surpervised
* UEBA, Malware behavior, ransomewaere attacks
* \- Reinforcement
* Problem types:
* Regression
* linear regression, logistic regression, polynomial regression, lasso regression
* clustering
* classification
* \- Web Traffic classification
* dimension reduction
* density estimation
* Famous algos
* SVM
* Bayesian networks
* decision trees
* random forests
* Hierarchical algos
* genetic algorithms
* ANN's
* Areas to focus (from aws)
  * Threat, intrusion and anomaly detection for cloud security
  * ML for malware analysis and detection
  * Finding security vulnerabilities using ML
  * Protecting and preserving data privacy in the cloud
  * Learning with limited/noisy labels and weakly supervised learning
  * Causal inference for information security
  * Graph modeling and anomaly detection on graphs
  * Zero/One-shot learning for information security
* *From <*[*https://www.amazon.science/research-awards/call-for-proposals/ai-for-information-security*](https://www.amazon.science/research-awards/call-for-proposals/ai-for-information-security)*>*
* The advent of the Internet of Things and the increasing dependence on digital technology have given rise to many security incidents in recent years. Data breaches, zero-day attacks, malware, ransomware, denial of service or DoS, phishing, and social engineering have progressed at near viral proportions. Cyber threats are outpacing the ability of cybersecurity to detect and prevent them. That’s where data science comes in.
* Cybersecurity is dedicated to protecting networks, computers, software programs, and data using various technologies and processes. Data science provides techniques used in machine learning, such as data modeling, statistical analysis, predictions, anomaly detection, forecasts, and pattern finding. Cybersecurity data science is a scientific, data-focused approach to identifying threats through machine learning. Leveraging the systems and processes of data science increases the ability to extract security incident insight and patterns from cybersecurity data for faster detection and a more robust, effective defense.
* *From <*[*https://divergence.one/data-science-cybersecurity/*](https://divergence.one/data-science-cybersecurity/)*>*
* Data Science Courses
* Where cybersecurity takes action, data science provides the analysis and vision. Machine learning-powered by data science techniques helps with anomaly detection by quickly scanning huge amounts of code to look for differences that could indicate malicious code. Penetration testing is also improved using automation and adaptive learning to test firewalls against intrusion. Data science empowers cybersecurity with information, speed, and accuracy that far surpasses what it has been able to do to date.
* [Data science courses](https://divergence.one/individuals-courses/) teach you the theory, tools, languages, and techniques widely used in the industry. Topics may include the following:
  * API Interactions
  * Computer Vision
  * Deep Learning (Neural Networks)
  * Ensemble Techniques & Model Tuning
  * Natural Language Processing (NLP)
  * PostgreSQL/pgAdmin
  * Python and R Programming for AI
  * Recommendation Systems
  * Statistics
  * Supervised and Unsupervised Learning
  * Recommendation Systems
  * Tableau, JavaScript, HTML5/CSS, and Git/GitHub
* *From <*[*https://divergence.one/data-science-cybersecurity/*](https://divergence.one/data-science-cybersecurity/)*>*
* Curriculum
* [Module 1: Foundations of Machine Learning for Security](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity#collapse-accordion-4082-1)
  * Introduction to supervised learning models
    * Logistic regression, Naive Bayes, neural networks, deep learning models
  * Introduction to unsupervised learning models
    * PCA, K-means, Gaussian mixture models
  * Live Demonstration: Building a machine learning pipeline
* [Module 2: Data-Driven Network and Computer Security](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity#collapse-accordion-4082-2)
  * Introduction to Internet architecture, measuring Internet traffic behavior and anomaly detection
  * Live Demonstration: Analyze internet network traffic using unsupervised learning techniques
  * Applications of machine learning to network security
    * Supervised learning examples: Spam filtering, phishing
    * Unsupervised learning examples: Anomaly detection
* [Module 3: Machine Learning in the Presence of Adversaries](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity#collapse-accordion-4082-3)
  * Introduction to adversarial machine learning, threat models
    * Example: Distorting personalization
  * Defending against adversaries
  * Example: Evading intrusion/attack detection
* [Module 4: Ethics, Fairness, Responsibility, and Transparency in Data-Driven Cybersecurity](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity#collapse-accordion-4082-4)
  * Fairness, Transparency, and Explainability in cybersecurity ML models
    * Privacy definitions and how to actualize privacy for cybersecurity applications in industry
    * Externalities and implications of errors in ML models for cybersecurity
  * Responsible data lifecycles
    * Hands-on lab focused on building a model to detect fraudulent accounts leveraging virtual case study
* [Module 5: Secure Machine Learning Development & Deployment](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity#collapse-accordion-4082-5)
  * Students have the option to develop a real or hypothetical cybersecurity machine learning deployment case study, culminating in personalized UChicago faculty feedback and guidance on your strategy.
* *From <*[*https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity*](https://professional.uchicago.edu/find-your-fit/professional-education/machine-learning-cybersecurity)*>*
* Dataingestion methods
* \- apache flume and kafka
* \- amzon kinesis
* Apache Sqoop, Apache Storm, Gobblin, Data Torrent, Syncsort, and Cloudera Morphline
* Frameworks
* threat hunting
* Mitre
* <https://www.fortinet.com/products/fortiai>
* <https://www.ibm.com/topics/threat-hunting>
* <https://threatcop.ai/blog/threat-hunting/>
* <https://www.recordedfuture.com/threat-intelligence/>
* <https://www.xenonstack.com/use-cases/threat-analytics>
* <https://awakesecurity.com/blog/network-threat-hunting-to-defend-the-broad-attack-surface/>
* <https://hackernoon.com/osint-tool-for-visualizing-relationships-between-domains-ips-and-email-addresses-94377aa1f20a>
* <https://medium.com/brim-securitys-knowledge-funnel/visualizing-ip-traffic-with-brim-zeek-and-networkx-3844a4c25a2f>
* <https://medium.com/brim-securitys-knowledge-funnel/hunting-emotet-with-brim-and-zeek-1000c2f5c1ff>
* <https://github.com/MarkBaggett/domain_stats>
* <https://client.rdap.org/?type=domain&object=dfwairport.com>
* <https://www.exabeam.com/explainers/siem/siem-analytics/>
* [https://builtin.com/artificial-intelligence/machine-learning-cybersecurityhttps://builtin.com/artificial-intelligence/machine-learning-cybersecurity](https://builtin.com/artificial-intelligence/machine-learning-cybersecurityhttps:/builtin.com/artificial-intelligence/machine-learning-cybersecurity)
  * Installation of Anaconda
  * Introduction on Python
  * Introduction to Pandas
  * Introduction to Jupyter
  * Math fundamentals for ML
  * Introduction to linear algebra
  * Introduction to Statistics
  * Introduction to probability
  * Introduction to scikit learning
  * Exploratory Data Analysis and visulization using Pandas
  * Data Engineering
    * Postgres sql
    * Mongo db
    * Csv
    * Api reading
  * Machine Learning Terminology
    * Super vised learning
    * Unsuper vised learning
    * Hybrid
  * Classification
  * Clustering
  * KNN
  * Model evaluation
  * Linear Regression
  * Logitic Regression
  * NLTK
  * Naïve Bayes classification
  * Decision trees
  * Ensemble Techniques
  * Dimension Reduction
  * Stochastic Gradient Descent
  * Neural Networks
  * Deep Learning
  * Recommendation Engine
  * Classification of malicious urls
* Phishing :
* Supervised learning algorithms such as Random Forest, SVM, MLP, KNN, and their stacked ensembles
* *From <*[*https://paperswithcode.com/paper/anomaly-detection-in-emails-using-machine*](https://paperswithcode.com/paper/anomaly-detection-in-emails-using-machine)*>*
* *
  * <https://machinelearningmastery.com/clustering-algorithms-with-python/>
  * <https://www.sans.org/cyber-security-courses/applied-data-science-machine-learning/>

Python code to find file hash and search on virustotal and alien vault, export api key as environmental variable

Python code to check file, check file header and  tell if it mz, pk, rar, elf.mac, %pdf. Mscf

PE header analysis

Find packed or unpacked

Base 64 encode detect and decode

## In this section

* ✅ [Installation](installation/README.md) · 2/2 pages written
* ✅ [Machine Learning](machine-learning.md)
* ✅ [Large Language Models (LLM)](large-language-models-llm.md)
* ✅ [Security Analytics](security-analytics.md)
* ✅ [AI Fundamentals & Azure AI](ai-fundamentals-and-azure-ai/README.md) · 6/6 pages written
