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

### External Interface Requirement

- **Input Format**: The system should accept network traffic data in JSON format
- 
## Dependencies

## Constraints

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