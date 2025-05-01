




Beyond Traditional Cryptography: 
An Adaptive Chaos-Based Encryption and AI-Driven Anomaly Detection Framework for Securing Real-Time Embedded Systems




Author: Sujith Kumar  
Affiliation: ________________________
Contact Number: +91 8892712235
E-mail ID: sujithkumar426@gmail.com















"BEYOND TRADITIONAL CRYPTOGRAPHY:
AN ADAPTIVE CHAOS-BASED ENCRYPTION AND AI-DRIVEN ANOMALY DETECTION FRAMEWORK FOR SECURING REAL-TIME EMBEDDED SYSTEMS”


Abstract
The increasing adoption of real-time embedded systems (RTES) and Internet of Things (IoT) devices has led to a surge in cyber threats, exposing critical vulnerabilities in conventional encryption and authentication mechanisms such as RSA, ECC, and AES, which have high computational overhead and are not quantum safe. This paper proposes an adaptive,  lightweight, and quantum-safe security framework integrating chaos-based encryption, true random number generators (TRNGs) ensuring unpredictability and high entropy, and a lightweight, machine learning-based intrusion detection system (IDS) to adapt the security mechanism dynamically to threats by modifying encryption parameters to mitigate risks in real time. This research lays the foundation for future developments in post-quantum cryptography and chaos-based security solutions for resource-constrained real-time systems.

Keywords:  
Chaos-based encryption, Post-quantum cryptography, Real-time embedded systems, Machine Learning-Based Anomaly Detection,  Low-Power Security Solutions, Adaptive Security Mechanisms

       1.   Introduction
The rapid growth of embedded systems and the Internet of Things (IoT) has revolutionized industries, enabling real-time automation, remote monitoring, and seamless connectivity across critical infrastructure, healthcare, industrial control systems (ICS), and consumer applications. With billions of IoT devices deployed globally, the embedded computing landscape is expanding at an unprecedented pace, offering efficiency, scalability, and data-driven intelligence. However, this rapid proliferation has also exposed significant security challenges. Unlike traditional computing systems, real-time embedded systems (RTES) and IoT devices operate under severe resource constraints—low power, limited computational capacity, and minimal security provisions—making them prime targets for cyber-attacks[1].

Traditional encryption methods like RSA, ECC, and AES are computationally expensive, making them unsuitable for low-power embedded systems. Additionally, these cryptographic techniques rely on mathematical complexity for security, but advances in quantum computing threaten to break these encryption schemes in the near future when better computational power is avilable. Authentication in RTES is another critical challenge. Man-in-the-middle (MITM) attacks, replay attacks, and firmware tampering are rising concerns, as IoT devices often lack robust identity verification mechanisms. Many security breaches occur due to static encryption keys, predictable authentication patterns, or weak cryptographic implementations.

Compromising an RTES or IoT device can have devastating real-world consequences which will increase in future with advancements. Healthcare Attacks: Hacked medical implants, insulin pumps, or pacemakers can be manipulated to harm patients and steal and manipulate the personal and critical details. Industrial & Smart Grid Threats: Cybercriminals targeting industrial control systems (ICS) can shut down power grids, disrupt factories, or sabotage oil pipelines. Automotive Security Threats: Connected vehicles rely on embedded ECUs for safety and navigation which have to be connected to the web but is under threat of cyber attacks. Smart Home & Consumer IoT Breaches: Weak authentication in smart locks, surveillance cameras, and voice assistants has led to home invasions and privacy violations.

To address these threats, a new security paradigm is needed—one that is: Lightweight and suitable for RTES with limited resources. Dynamic & Adaptive to responds to real-time threats. Unpredictable & Non-Deterministic which is quantum-safe. This paper proposes an adaptive, chaos-based encryption and authentication framework, integrating true random number generation (TRNG), machine learning anomaly detection, and post-quantum cryptography (PQC). This approach aims to enhance security while maintaining efficiency for real-time embedded systems in mission-critical environments.

       1.   Review of Literature
The security challenges faced by real-time embedded systems (RTES) and IoT devices have led to extensive research into lightweight cryptography, chaos-based encryption, anomaly detection, and post-quantum cryptography. This section reviews the existing literature on these topics and identifies gaps that this research aims to address.

The proliferation of Internet-of-Things (IoT) devices has led to an alarming increase in cyberattacks targeting these systems. According to Seals (2021) [1], IoT-based cyberattacks more than doubled in the first half of 2021, reaching 1.5 billion incidents, up from 639 million in the previous six months. Attackers exploit IoT devices for various malicious activities, including data theft, cryptocurrency mining, and botnet formation. The study, based on Kaspersky’s telemetry data, highlights the growing vulnerabilities in smart devices due to their always-on connectivity, weak authentication mechanisms, and lack of regular security updates. These findings reinforce the urgent need for adaptive security models, such as machine learning-driven anomaly detection and chaos-based encryption, to counteract emerging threats in real-time embedded systems and IoT networks. A 2025 incident exposed 2.7 billion records, marking one of the most extensive IoT data leaks to date (Mascellino, 2025)[2]. 

Traditional security models rely on predefined encryption schemes that do not adapt dynamically to real-time threats, making them vulnerable to zero-day exploits[3]. Authentication in RTES is often static and predictable, allowing attackers to bypass weak identity verification mechanisms using replay attacks and MITM attacks.

Limitations of Traditional Cryptographic Techniques: Existing encryption methods, such as RSA, ECC, and AES, rely on deterministic mathematical problems, such as prime factorization and elliptic curve calculations, for security. While these methods are robust today, research warns that: Quantum computers will eventually break RSA and ECC encryption using Shor’s algorithm, making them obsolete[]. Computational complexity in asymmetric encryption leads to high power consumption, making it unsuitable for resource-constrained RTES[]. Traditional cryptography lacks dynamic adaptation, meaning it does not adjust to real-time security threats and used to analyse the network but not adapt it to need.

Chaos-Based Cryptography for Unpredictability: Chaotic systems, such as logistic maps, Lorenz attractors, and Chua’s circuits, exhibit high sensitivity to initial conditions, making them excellent candidates for pseudo-random number generation (PRNG) in cryptographic applications. Research has demonstrated that: Chaos-based encryption algorithms can generate high-entropy keys that are computationally infeasible to predict[]. Chaotic systems offer lower computational cost compared to RSA and ECC while maintaining high security[]. The 3D chaotic attractor models have been successfully used for image encryption and secure communications, proving their feasibility in embedded applications[].

Machine Learning-Based Anomaly Detection for Security: AI and ML techniques have been widely studied for intrusion detection and network anomaly detection, showing significant improvements in identifying cyber threats in real-time. Research highlights that:
Deep learning models (CNNs, RNNs) can accurately detect malicious traffic in IoT networks[]. Unsupervised learning techniques, such as autoencoders and clustering algorithms, can identify previously unknown attack patterns[]. Integrating ML with cryptographic security mechanisms has been proposed to dynamically adjust encryption parameters based on detected anomalies[].

Post-Quantum Cryptography (PQC) and Future-Proof Security: To address the threat of quantum computing, researchers have proposed post-quantum cryptographic (PQC) algorithms, such as: Lattice-based encryption (NTRU, Kyber) – Resistant to Shor’s algorithm and suitable for constrained devices. Hash-based signatures (SPHINCS+) – Provide quantum-resistant authentication with lightweight implementations. Code-based cryptography (McEliece algorithm) – Offers long-term security but requires large key sizes.
       
       1.   Research Gap
While research has explored chaos-based encryption, ML-based anomaly detection, and PQC separately, there is no unified approach that: Uses chaos-based cryptographic techniques for lightweight and non-deterministic encryption capable of securing RTES without excessive computational overhead. Incorporates integrating machine learning-driven anomaly detection to dynamically adjust encryption parameters based on real-time threats. Ensures quantum resistance through integration with post-quantum cryptographic methods optimized for RTES and IoT Intgration.
       
       1.   Research Objectives
The primary objective of this research is to develop a lightweight, adaptive encryption and authentication framework for real-time embedded systems (RTES) and IoT devices that enhances security while minimizing computational overhead. This research aims to address the limitations of traditional cryptographic methods by integrating chaos-based cryptography, machine learning-driven anomaly detection, and quantum-resistant techniques.

The Research Objectives can be broken into five Specific Objectives:  To analyze the limitations of existing encryption and authentication mechanisms in RTES and IoT, focusing on their computational overhead, predictability, and susceptibility of devices to attacks.
To explore and evaluate chaos-based encryption techniques, such as logistic maps, Lorenz attractors, and chaotic pseudo-random number generators (CPRNGs), for enhancing encryption unpredictability and randomness of the encryption for enhanced device security.
To integrate a machine learning (ML)-based anomaly detection model that monitors real-time network activity, detects potential cyber threats, and dynamically adjusts encryption parameters to strengthen security for the threat in real time and minimize severity or prevent. 

To design a lightweight, adaptive security framework that incorporates True random number generation (TRNG), Chaos-based cryptographic techniques and ML-driven security adaptation to dynamically respond to threats. To evaluate the proposed framework’s feasibility and effectiveness by comparing its performance (security strength, computational efficiency, adaptability) with traditional encryption methods in embedded environments. By achieving these objectives, this research aims to contribute a novel, quantum-resistant, real-time security mechanism for embedded and IoT devices that is both efficient and robust against evolving cyber threats.

       1.   Proposed Methodology
The proposed adaptive encryption and authentication framework is designed to secure real-time embedded systems (RTES) and IoT devices by integrating chaos-based cryptographic key generation, machine learning-based anomaly detection, and post-quantum authentication. 
The system architecture consists of three primary components: A Chaotic Key Generation and Encryption Mechanism – Ensuring lightweight and unpredictable encryption system. 
An AI-Driven Anomaly Detection and Adaptive Security – Dynamically adjusting encryption parameters based on detected threats. A Quantum-Resistant Authentication – Preventing unauthorized access and ensuring future-proof security even agains quantum systems.

Chaotic Key Generation and Encryption Mechanism: The encryption process is based on chaotic systems, which exhibit high sensitivity to initial conditions and generate unpredictable key sequences. The system is structured into three main components: 
True Random Number Generation (TRNG) for Initial Seed. Chaos-Based Pseudo-Random Number Generator (CPRNG). Lightweight Encryption Process.

A True Random Number Generator (TRNG) collects entropy from real-world physical sources like sensor noise, electronic fluctuations, environmental changes etc to produce a highly random seed which serves as the starting input for initializing the chaotic system to generate encryption keys. Using chaotic systems like Logistic Map, Lorenz Attractor, or Chua’s Circuit, a chaotic key stream is generated. The key stream is non-repeating and unpredictable, making it resistant to attacks. The chaotic system ensures non-periodicity, high sensitivity to initial conditions, and deterministic unpredictability—making it ideal for lightweight encryption in RTES. The plaintext data is encrypted using Bitwise XOR operations with the chaotic key stream. Chaotic substitution and permutation techniques for increased diffusion and confusion. Since chaotic maps are computationally inexpensive, this method is well-suited for RTES with limited processing power.

AI-Driven Anomaly Detection and Adaptive Security: To provide real-time intrusion detection and adaptive security, a lightweight AI model is integrated, ensuring minimal computational overhead for RTES. A Lightweight Machine Learning-Based Intrusion Detection is a compact, pre-trained model acts as anomaly detection model continuously monitors system activity while ensuring minimal computational overhead for RTES. They analyze: Network traffic behavior for deviations from usual expected network patterns. System operation logs to detect unusual activity or privilege escalation. Strang or Excessive Power and computation usage which might indicate a potential side-channel attack.

Suitable lightweight models that can be used without adding too much overhead  to the system process are: Autoencoders (AE) - Small neural networks that reconstruct normal data patterns and flag deviations as anomalies. Long Short-Term Memory (LSTM) - Based Models Efficient recurrent models that track temporal patterns in system logs to detect stealthy attacks. One-Class Support Vector Machines (One-Class SVM) - A non-deep learning method that learns normal system behavior and flags anything outside it. Isolation Forest (iForest) - A tree-based model that efficiently isolates outliers in real-time. These models can be optimized for low-power devices through pruning, quantization, and model distillation to ensure fast, memory-efficient intrusion detection.

Adaptive Encryption Parameter Adjustment: If an anomaly is detected, the system dynamically modifies encryption parameters to mitigate threats by taking actions by: Reinitializing chaotic key generation with a new TRNG seed for added unpredictability. Altering chaotic map parameters (e.g., logistic map, Lorenz attractor) to generate a new key stream. Increasing encryption complexity proportionally to attack severity or Switching authentication methods if suspicious activity is detected in identity validation.

Reinforcement Learning for Self-Optimizing Security: A lightweight reinforcement learning (RL) model (e.g., Deep Q-Network (DQN) with reduced parameter size) fine-tunes security settings over time as it learns geral pattern. The model analyzes past attack patterns and dynamically optimizes encryption and authentication configurations and Minimizes computational overhead by selecting the most efficient security response for detected threats.

Quantum-Resistant Authentication and Key Exchange is used To ensure secure access control and tamper-proof key exchange, the system integrates post-quantum cryptography (PQC) techniques. Authentication is done via Post-Quantum Cryptography (PQC) systems using lattice-based cryptographic methods (e.g., Kyber, NTRU) to verify device identities. Hash-based digital signatures (SPHINCS+) ensure tamper-proof authentication without relying on conventional RSA/ECC keys. Secure Key Exchange Using Chaotic Sequences where encryption keys are derived from chaotic sequences, making them unique for each session and resistant to replay attacks. A shared chaotic parameter is securely exchanged using PQC-based key encapsulation mechanisms (KEMs).

Session-Based One-Time Authentication Tokens: The chaotic key generation system is used to generate one-time authentication tokens that are non-reproducible due to their sensitivity to initial conditions. These tokens replace static passwords or pre-shared keys, and they expire after each session making authentication highly secure and resistant to replay attacks.

       1.   Analysis and Interpretations
Lightweight, Non-Deterministic chaos-based cryptography ensures low overhead and unpredictability. Quantum-Safe PQC based Authentication Future-proofs security against both classical and quantum attacks. Secure Key Exchange Using Chaos Theory Eliminates reliance on traditional key distribution. AI Driven Real-Time Adaptive Security enables self-adjusting encryption mechanisms and through Reinforcement learning improves defenses over time providing Self-Optimizing Security.

Security Strength Against Classical & Quantum Attacks
.
.
.
Key Entropy & Unpredictability of Chaotic PRNGs: Chaotic PRNGs exhibit high entropy, non-linearity, and sensitivity to initial conditions, ensuring that: The generated keys are unpredictable and unique for each session. Even minimal variations in input produce vastly different outputs, making cryptanalysis infeasible. No polynomial-time algorithms exist to reverse-engineer the chaotic sequence. Traditional encryption relies on mathematical complexity, making it vulnerable to predictive attacks with advancements in computing. 

Resistance to Classical Attacks like Brute Force Attacks: Unlike AES-256 or RSA-4096, where key search spaces are defined, chaotic keys evolve dynamically, making exhaustive search impractical. Side-Channel Attacks: Low computational footprint reduces the system’s power and timing signature, minimizing vulnerability to side-channel attacks.
Statistical & Cryptanalysis Attacks: Key generation does not follow a fixed, deterministic pattern based on, preventing frequency-based attacks.

Resistance to Quantum Attacks: The proposed method does not rely on factorization or discrete logarithms, rendering Shor’s algorithm ineffective. Grover’s algorithm speeds up key searches, but chaotic keys are not stored statically and evolve dynamically. Have a randomized key schedule, mitigating quadratic search efficiency. Using post-quantum cryptographic schemes (e.g., lattice-based, hash-based) for authentication eliminates dependence on RSA/ECC, ensuring security even in a quantum era.

Performance Comparison with RSA/ECC/AES:  One of the critical concerns in RTES security is computational overhead. The proposed system ensures minimal impact on processing power, memory, and energy consumption than RSA/ECC, making it viable for low-power IoT/RTES. No large matrix operations or modular exponentiations, reducing CPU overhead. Adaptive encryption strength, allowing dynamic trade-offs between security and performance. Efficient key exchange using chaotic synchronization, eliminating heavy cryptographic computations.





Metric	RSA-4096	ECC-521	AES-256	Proposed Chaotic Encryption
Key Size (bits)	4096	521	256	128-256 (dynamic)
Encryption Time	High	Moderate	Low	Very Low
Decryption Time	High	Moderate	Low	Very Low
Computational Complexity	Exponential	Polynomial	Logarithmic	Logarithmic
Quantum Resistance	No	No	Partially	Yes
Adaptability	No	No	No	Yes (ML-driven)

Case Studies & Simulations for Adaptability against Cyber Threats: The integration of AI-driven anomaly detection enhances the system’s adaptability to evolving cyber threats.
Scenario 1 - Man-in-the-Middle (MITM) Attack Prevention:  Anomaly detection identifies unusual packet timing and handshake irregularities. Adaptive encryption switches to a more complex chaotic function for added security.
Scenario 2 - Replay Attack Defense: Chaotic key generation ensures that each session key is unique preventing the reuse of old keys.
Scenario 3 - AI-Based Intrusion Detection: The system monitors network flow deviations using an autoencoder-based anomaly detector. If an attack pattern emerges, the model retrains dynamically, improving future threat detection. If an advanced attack is detected, the system can: Regenerate chaotic seeds to alter encryption keys. Adjust authentication mechanisms (e.g., requiring multi-factor authentication). Modify system behavior in real-time to counteract new threats.

       1.   Limitations of the Proposed Approach
While the proposed system offers strong encryption, adaptive security, and computational efficiency, it faces the following limitations:
Hardware Constraints: Many RTES and IoT devices operate on low-power microcontrollers with limited computational resources. Implementing chaotic key generation and AI-driven anomaly detection may require dedicated cryptographic accelerators or hardware optimization.
Algorithm Complexity & Optimization: While chaos-based encryption is computationally lightweight, ensuring real-time performance requires fine-tuning of chaotic functions. Certain chaotic maps (e.g., Lorenz attractor) require floating-point precision, which may not be available on all RTES architectures.

Key Synchronization Issues: Challenge in Securely Synchronizing Chaotic PRNGs: Unlike traditional encryption, where keys are statically defined, chaotic systems require both sender and receiver to remain synchronized with the same initial conditions. Network delays, packet loss, or external interference may cause desynchronization, leading to decryption failures.

Side-Channel Attacks on IoT Devices: Although chaotic encryption minimizes computational signatures, power analysis attacks could still infer encryption patterns from hardware leakage. AI-Based Adversarial Attacks on Anomaly Detection: Attackers could use adversarial ML techniques to manipulate the anomaly detection model, reducing its ability to detect cyber threats.

Potential Improvements:  To address the above limitations, the following improvements can enhance the security, efficiency, and scalability of the system:
Exploring Hardware-Optimized Chaotic Encryption for IoT Security: Current IoT security solutions rely on software-based encryption, which adds latency and energy overhead. Hardware-optimized chaotic PRNGs and authentication modules can significantly improve: Throughput & power efficiency in IoT devices. Resistance to physical tampering & side-channel attacks.

Exploring error-correction mechanisms and using self-recovering chaotic synchronization techniques by Combining Chaos-Based Encryption with Zero-Trust Architectures (ZTA): Zero-Trust Architectures enforce continuous verification, ensuring chaotic encryption keys and authentication parameters are dynamically revalidated. Enhancing AI-Driven Threat Adaptability: Current systems monitor traffic and adapt encryption parameters. However, further improvements can be made by: Reinforcement Learning for self-healing security. Federated Learning for decentralized threat intelligence, where RTES and IoT devices can collaboratively learn from distributed cyber threat patterns. 
Research on Quantum-Resistant Authentication Schemes: Exploring quantum-secure Lattice-based signatures for RTES authentication to prepare and secure for the Post Quantum security. The convergence of chaos theory, AI-driven security, and post-quantum cryptography presents an exciting frontier in real-time embedded system security. Future research will be crucial in making these theoretical advancements practically deployable for securing next-generation IoT and RTES environments.

       1.   Conclusion
The rapid proliferation of real-time embedded systems (RTES) and IoT devices has introduced unprecedented cybersecurity challenges, particularly in ensuring lightweight, adaptive, and quantum-resistant encryption. Traditional encryption methods, such as RSA and ECC, rely on mathematical complexity for security, but they face significant computational overhead and are vulnerable to future quantum attacks. Moreover, static cryptographic approaches struggle to provide real-time adaptability against evolving cyber threats. To address these limitations, this paper proposed an integrated security framework that combines: Chaos-based encryption for lightweight, high-entropy, and quantum-safe cryptographic protection. AI-driven anomaly detection for real-time adaptation against network intrusions and cyber threats. Dynamic authentication mechanisms that ensure secure device interaction and prevent unauthorized access.

1.   References

[1] Seals, T. (2021, September 6). IoT attacks skyrocket, doubling in 6 months. Threatpost. https://threatpost.com/iot-attacks-doubling/169224/

[2] Mascellino, A. (2025, February 12). Massive IoT data breach exposes 2.7 billion records. Infosecurity Magazine. https://www.infosecurity-magazine.com/news/iot-data-breach-exposes-27-billion/

[3] Farah, T., & Alshammari, B. M. (2023). A novel image encryption scheme based on a new hyperchaotic map. Multimedia Tools and Applications. Springer. https://doi.org/10.1007/s11042-023-16873-x

[4] Ahvanooey, M. T., et al. (2022). Modern authentication schemes in smartphones and IoT devices: An empirical survey. IEEE Internet of Things Journal, 9(10), 7639-7663. https://doi.org/10.1109/JIOT.2021.3138073

[5] Kumar, A., & Mishra, A. (2022). LWE-Based Quantum-Resistant Pseudo-Random Number Generator. International Arab Journal of Information Technology, 20(6). https://doi.org/10.34028/iajit/20/6/8

[6] Sama, A., Meyliana, Heryadi, Y., & Sahroni, T. R. (2024). Lightweight Pseudo Random Number Generator for Embedded Systems. International Journal of Safety and Security Engineering, 14(4). https://doi.org/10.18280/ijsse.140409

[7] Dehkordi, I. F., Manochehri, K., & Aghazarian, V. (2023). Internet of Things (IoT) Intrusion Detection by Machine Learning (ML): A Review. Asia-Pacific Journal of Information Technology and Multimedia, 12(1), 13–38. https://doi.org/10.17576/apjitm-2023-1201-02

[8] Opiłka, F., Niemiec, M., Gagliardi, M., & Kourtis, M.A. (2024). Performance Analysis of Post-Quantum Cryptography Algorithms for Digital Signature. Applied Sciences, 14(12), 4994. https://doi.org/10.3390/app14124994

[]  Sajimon, P. C., Jain, K., & Krishnan, P. (2022). Analysis of post-quantum cryptography for Internet of Things. In Proceedings of the 6th International Conference on Intelligent Computing and Control Systems (ICICCS 2022) IEEE. https://doi.org/10.1109/ICICCS53718.2022.9787987

[] Hwang, J., Kale, G., Patel, P. P., Vishwakarma, R., Aliasgari, M., Hedayatipour, A., Rezaei, A., & Sayadi, H. (Year). Machine learning in chaos-based encryption: Theory, implementations, and applications. [Journal/Conference Name], Volume(Issue), [page numbers]. https://doi.org/[DOI if available]

Onuki, K., Cho, K., Horio, Y., & Miyano, T. (2022). Secret-key exchange through synchronization of randomized chaotic oscillators aided by logistic hash function. IEEE Transactions on Circuits and Systems I: Regular Papers, 69(4), 1655–1668. https://doi.org/[DOI if available]

Radanliev, P., De Roure, D., & Santos, O. (2023, September 17). Red teaming generative AI/NLP, the BB84 quantum cryptography protocol and the NIST-approved quantum-resistant cryptographic algorithms. arXiv. https://doi.org/10.48550/arXiv.2310.04425

El Hadj Youssef, W., Abdelli, A., Kharroubi, F., Dridi, F., Khriji, L., Ahshan, R., Machhout, M., Nengroo, S. H., & Lee, S. (2023, November). A secure chaos-based lightweight cryptosystem for the Internet of Things. ResearchGate. Retrieved from https://www.researchgate.net/publication/375594998_A_Secure_Chaos-Based_Lightweight_Cryptosystem_for_the_Internet_of_Things

Jain, K., Titus, B., Krishnan, P., & Sudevan, S. (2024). A lightweight multi-chaos-based image encryption scheme for IoT networks. IEEE Access, PP(99), 1-1. https://doi.org/10.1109/ACCESS.2024.3377665

Alkhonaini, M., Alenizi, F. A., Jazyah, Y. H., & Lee, S. (2024). A two-phase spatiotemporal chaos-based protocol for data integrity in IoT. Scientific Reports, 14(1). https://doi.org/10.1038/s41598-024-58914-x

Abd El-Latif, A. A., Ramadoss, J., Abd-El-Atty, B., Khalifa, H. S., & Nazarimehr, F. (2022). A novel chaos-based cryptography algorithm and its performance analysis. Mathematics, 10(14), 2434. https://doi.org/10.3390/math10142434


Joseph, D., Misoczki, R., Manzano, M., Tricot, J., Pinuaga, F. D., Lacombe, O., Leichenauer, S., Hidary, J., Venables, P., & Hansen, R. (2022). Transitioning organizations to post-quantum cryptography. Nature, 605, 237–243. https://doi.org/10.1038/s41586-022-04623-2

Jallouli, O. (2017). Chaos-based security under real-time and energy constraints for the Internet of Things [Doctoral dissertation, Université de Nantes]. HAL Open Science. https://hal.science/tel-01633910v1

National Institute of Standards and Technology (NIST). (2024). Module-lattice-based digital signature standard (FIPS 204). U.S. Department of Commerce. https://doi.org/10.6028/NIST.FIPS.204

