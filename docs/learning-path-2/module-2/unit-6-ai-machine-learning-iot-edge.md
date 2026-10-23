# Learning Path 2 — Module 2, Unit 6: Describe AI, machine learning, and IoT/Edge services in Azure

**Learning path:** Introduction to Cloud Infrastructure — Describe Azure architecture and services  
**Module:** Describe Azure compute services  
**Estimated study time:** 8–10 minutes

## Learning objectives

By the end of this lesson, you should be able to:
- Distinguish artificial intelligence (AI), machine learning (ML), and Internet of Things (IoT).
- Recognize Azure services used for AI, machine learning, and IoT/edge scenarios.
- Explain at a high level why some processing happens near a device rather than only in the cloud.
- Choose a plausible service category for a simple scenario.

## 1. Start with a familiar example

Imagine a school wants to monitor water storage. A sensor measures the water level in a tank and sends readings to a system. The school wants to:
- see current and historical readings;
- receive an alert when the tank is nearly empty;
- predict when the tank may run out;
- perhaps use a camera to identify a leaking pipe.

Different technologies help with different parts of this task. Sensors collect observations; IoT systems connect and manage devices; cloud services store and process data; machine learning can identify patterns; and AI services can support tasks such as image or language analysis.

## 2. AI and machine learning

**Artificial intelligence (AI)** is a broad field focused on systems that perform tasks associated with human-like capabilities, such as understanding language, recognizing images, or making recommendations.

**Machine learning (ML)** is one approach within AI. Instead of writing every rule manually, developers train a model to identify patterns from examples or data and use those patterns to make predictions or classifications.

For example:
- A fixed rule sends an alert whenever the tank reading falls below 15%.
- A machine-learning model could use past usage patterns to estimate when the tank will run out.
- An image-analysis AI service could help identify visible damage in a photograph.

Azure offers AI and machine-learning services, including Azure AI services for ready-made AI capabilities and Azure Machine Learning for building, training, managing, and deploying machine-learning models. Service names and capabilities can evolve, so focus on the role each service performs rather than memorizing every product feature.

## 3. Internet of Things (IoT)

The **Internet of Things** describes physical devices—such as sensors, meters, cameras, and machines—that collect or exchange data over a network.

An IoT solution commonly involves:
1. **Devices and sensors** that measure or produce data.
2. **Connectivity** that sends the data to another system.
3. **Device management and ingestion** to connect devices securely and handle their messages.
4. **Storage and processing** to make the data useful.
5. **Applications, dashboards, or alerts** that people use to act on the information.

IoT is not just “a sensor connected to Wi-Fi.” A complete solution also considers device identity, secure communication, data handling, monitoring, and what should happen when readings indicate a problem.

## 4. What does edge computing mean?

**Edge computing** means processing data closer to where it is generated—on or near the device—rather than sending every task to a distant cloud service first.

For the school water tank:
- The sensor can send readings to Azure for dashboards and long-term analysis.
- A nearby gateway can filter readings or continue a basic local action if internet connectivity is temporarily unavailable.
- The cloud can analyze trends across several tanks and notify staff.

Edge processing can help reduce delay, limit the amount of data sent over a network, and support some operations when connectivity is unreliable. It does not mean that all cloud services become unnecessary.

## 5. Azure services: recognize the roles

| Service or category | Main role |
|---|---|
| Azure AI services | Ready-made AI capabilities, such as vision, speech, or language tasks |
| Azure Machine Learning | Build, train, manage, and deploy machine-learning models |
| Azure IoT Hub | Securely connect and communicate with IoT devices and ingest device messages |
| Azure IoT Operations / edge capabilities | Support data processing and operations closer to where industrial IoT data is produced; exact options depend on the solution and current Azure offerings |
| Azure Functions | Run event-driven code—for example, process a message or trigger an alert |
| Azure storage and analytics services | Store readings and analyze them over time |

These categories can work together. They are not interchangeable: IoT connectivity manages device communication, machine learning develops predictive models, AI services provide particular AI capabilities, and Functions can execute code in response to events.

## 6. Choose the right approach

- **Need to connect and manage many sensors?** Consider an IoT device connectivity and management service such as Azure IoT Hub.
- **Need to estimate future water use from historical readings?** Consider a machine-learning solution.
- **Need to analyze a photo for visible damage?** Consider an appropriate AI vision capability.
- **Need to run a small task when a new reading arrives?** Azure Functions may be suitable.
- **Need a fast local response even when connectivity is unreliable?** Consider edge processing for the time-critical part, while using cloud services for broader reporting and analysis.

A real solution may combine several of these options.

## 7. Knowledge check

**Question 1.** A farm uses sensors to report soil moisture. What does IoT primarily describe here?

A. A way to design a presentation  
B. Physical devices that collect and exchange data over a network  
C. A type of cloud billing account  

**Answer:** B. IoT involves connected physical devices and the data they produce or exchange.

**Question 2.** A model uses past tank readings to predict when the tank will run out. Which concept best describes the prediction approach?

A. Machine learning  
B. A resource group  
C. Azure DNS  

**Answer:** A. Machine learning can learn patterns from historical data and use them to make predictions.

**Question 3.** Why might a solution process some data at the edge?

A. To ensure that no cloud service can ever be used  
B. To reduce delay or continue a local operation when connectivity is limited  
C. To replace device security  

**Answer:** B. Edge processing can support low-latency or connectivity-sensitive tasks; it does not remove the need for security.

**Question 4.** Which service category is primarily associated with securely connecting IoT devices and handling their messages?

A. Azure IoT Hub  
B. Azure Pricing Calculator  
C. Azure Policy  

**Answer:** A. Azure IoT Hub provides IoT device connectivity and message-handling capabilities.

## Key takeaways

- AI is the broad field; machine learning is one approach within AI.
- IoT connects physical devices that collect and exchange data.
- Edge computing processes some data near where it is produced.
- Azure AI services, Azure Machine Learning, IoT services, Functions, and storage/analytics can play different roles in one solution.
- Choose services based on the problem to solve, not just the product names.

## Official learning resources

- [Describe AI, machine learning, and IoT/Edge services in Azure — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/)
- [AZ-900 study guide — Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)

*Service names and available features can change. Check current Microsoft Learn documentation when implementing a real solution.*
