# Phase 1: Planning and Research

## Scope 

The purpose of this program is to assist common users to detect threats

## Definitions

1. **Distributed Denial-of-Service (DDoS)**: A malicious attempt to disrupt the normal functioning of a targeted server, service, or network by overwhelming the target or its surrounding infrastructure with a flood of internet traffic. [1]
2. **Phishing**: An attempt to steal sensitive information, typically including usernames, passwords, credit card numbers, bank account details, or other critical data, with the intent to exploit or sell the stolen information. [2]
3. **Malware Traffic**: Any suspicious link, file, or connection created or received over the network. Malicious traffic poses a threat that can lead to incidents, potentially compromising an organization's security or affecting your personal computer. [3]
4. **Port Scanning Attack**: They scope out their target environment by sending packets to specific ports on a host, using the responses to identify vulnerabilities and determine which services and service versions are running on the host. [4]

## Requirement 

### Functional Requirement

- The system shall accept network traffic data in JSON or CSV format.
- The system shall preprocess input data before analysis.
- The system should be able to detect common network threats (DDoS, phishing, malware).
- The system should identify the type of detected threat (optional).
- The system should expose REST API endpoints for prediction.
- The system shall log all analyzed traffic and prediction results.
- The system shall generate alerts for detected threats.
- The system shall load and use a trained ML model.
- The system should identify and respond to suspicious usage patterns.

### Performance Requirement

- The system shall respond to prediction requests within 1 second.
- The system should handle at least 50 requests per second.
- The system shall achieve at least 90% detection accuracy.
- The system should maintain high recall to minimize missed attacks.
- The system should support scalability using Docker.
- The system shall operate within acceptable CPU and memory limits.
- The system should maintain 99% uptime.
- The system shall maintain stable performance under moderate load.
- Model inference shall complete within 200 ms.
- Logging shall not degrade system performance significantly.

### External Interface Requirement

- **Input Format**: The system should accept network traffic data in JSON format
- 
## Dependencies
- **Python Libraries**:
  - Flask: for serving the machine learning model via an API.
  - scikit-learn: for training machine learning models (e.g., decision trees, SVM).
  - (add more in future)
  
- **Datasets**:
  - CICIDS dataset (for network traffic analysis).
  - (add more in future)

- **Cloud Infrastructure (Mostly not deployed)**:
  - AWS EC2: for hosting and computation.


## Constraints

- **Data Availability**: High-quality and labeled network traffic data, especially aiming for specific types of attacks like DDoS.
- **Latency Constraints**: The system must process and respond to incoming network traffic data in real-time, which may require performance optimizations in both the model and the backend.
- **Resource Limitations**: If deploying on resource-limited devices, ensure that the machine learning models are optimized for efficiency, with low memory and CPU usage (make sure regularly computer can run this).

## Attributes

- **Accuracy**: The primary attribute for model performance. Should strive for 80%+ on test datasets.
- **Scalability**: The system should be scalable to handle large network traffic datasets and be deployable on cloud services. (note that this is a group project and mostly cloud services is a paid service, we will decide it in future)
- **Security**: Given the nature of the project, the system must follow security best practices, including secure communication (SSL), proper authentication/authorization, and protection against possible attacks on the detection system itself (e.g., data poisoning, adversarial attacks).
- **Usability**: The system should be easy to use for security professionals, with simple API endpoints and potentially a user interface for monitoring threats.
- **Modularity**: The system should be modular so that components such as the machine learning model, backend API, and alerting system can be updated independently.



## References

[1]: https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/
[2]: https://www.cloudflare.com/learning/access-management/phishing-attack/
[3]: https://home.sophos.com/en-us/security-news/2020/undetected-malicious-traffic
[4]: https://www.extrahop.com/resources/attacks/malicious-port-scanning