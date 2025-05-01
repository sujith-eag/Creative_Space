  

  

  

**Beyond Traditional Cryptography:**

**An Adaptive Chaos-Based Encryption and AI-Driven Anomaly Detection Framework for Securing Real-Time Embedded Systems**

  

  

  

  

**Sujith Kumar**

Student

Master of Computer Applications

Ramaiah Institute of Technology

Email: [sujithkumar426@gmail.com](mailto:sujithkumar426@gmail.com)

  

Dr. D Evangelin Geetha

Professor

Master of Computer Applications

Ramaiah Institute of Technology

Email: [degeetha@msrit.edu](mailto:degeetha@msrit.edu)

  

  

  

  

  

  

  

  

  

  

  

  

  

**BEYOND TRADITIONAL CRYPTOGRAPHY:**

**AN ADAPTIVE CHAOS-BASED ENCRYPTION AND AI-DRIVEN ANOMALY DETECTION FRAMEWORK FOR SECURING REAL-TIME EMBEDDED SYSTEMS**

  

  

  

**1. Abstract**

  

With the growing adoption of real-time embedded systems (RTES) and Internet of Things (IoT) devices, cyber security threats have significantly increased, revealing critical weaknesses in traditional encryption and authentication methods such as RSA, ECC, and AES. These conventional algorithms not only impose high computational overhead but also lack quantum resistance. This paper introduces a lightweight, adaptive, and quantum-secure security framework that integrates chaos-based encryption, true random number generators (TRNGs) to ensure high-entropy, non-deterministic key generation, providing a computationally efficient alternative to conventional cryptographic methods, and an efficient machine learning-driven intrusion detection system (IDS) which dynamically adjusts encryption parameters in response to detected threats, thereby enabling real-time risk mitigation. This research contributes to the advancement of post-quantum cryptography and chaos-based security approaches to strengthen security in next-generation embedded and IoT environments and resource-constrained real-time systems.

  

  

Keywords: **Chaos-based encryption, post-quantum cryptography, real-time embedded systems security, machine learning-based intrusion detection, adaptive cryptography, low-power security.**

  

  

  

  

  

**2. Introduction**

  

The rapid growth of embedded systems (RTES) and the Internet of Things (IoT) has revolutionized industries, enabling real-time automation, remote monitoring, and seamless connectivity across critical infrastructure, healthcare, industrial control systems (ICS), and consumer applications. With billions of IoT devices deployed globally, the embedded computing landscape is expanding at an unprecedented pace and due to their increased connectivity but unlike traditional computing systems their resource constraints—low power, limited computational capacity, and minimal security provisions—has exposed significant security challenges and made them prime-targets for cyber-attacks. The proliferation of Internet-of-Things (IoT) devices has led to an alarming increase in cyberattacks targeting these systems. According to _Seals (2021)_ [1], IoT-based cyberattacks more than doubled in the first half of 2021, reaching **1.5 billion incidents**, up from 639 million in the previous six months. Attackers exploit IoT devices for various malicious activities, including **data theft, cryptocurrency mining, and botnet formation**. The study, based on Kaspersky’s telemetry data, highlights the growing vulnerabilities in smart devices due to their **always-on connectivity, weak authentication mechanisms, and lack of regular security updates**. These findings reinforce the urgent need for **adaptive security models**, such as machine learning-driven anomaly detection and chaos-based encryption, to counteract emerging threats in real-time embedded systems and IoT networks. In **2025, an IoT data breach incident exposed 2.7 billion records of IP, passwords and names**, making it one of the most extensive IoT data leaks to date _(Mascellino, 2025)_[2].

  

Traditional encryption methods like RSA, ECC, and AES are computationally expensive, making them unsuitable for low-power embedded systems. Additionally, these cryptographic techniques rely on deterministic mathematical structures complexity for security, but advances in quantum computing threaten to break these encryption schemes in the near future making them vulnerable. Authentication in RTES is another critical challenge. Man-in-the-middle (MITM) attacks, replay attacks, and firmware tampering are rising concerns, as IoT devices often lack robust identity verification mechanisms. Many security breaches occur due to static encryption keys, predictable authentication patterns, or weak cryptographic implementations.

  

Compromising an RTES or IoT device can have devastating real-world consequences which will increase in future with advancements. Healthcare Attacks: Hacked medical implants, insulin pumps, or pacemakers can be manipulated to harm patients and steal and manipulate the personal and critical details. Industrial & Smart Grid Threats: Cybercriminals targeting industrial control systems (ICS) can shut down power grids, disrupt factories, or sabotage oil pipelines. Automotive Security Threats: Connected vehicles rely on embedded ECUs for safety and navigation which have to be connected to the web but is under threat of cyber attacks. Smart Home & Consumer IoT Breaches: Weak authentication in smart locks, surveillance cameras, and voice assistants has led to home invasions and privacy violations. To address these threats and limitations in traditional security approaches, there’s a need for new security paradigm—one that is: Lightweight and suitable for RTES with limited resources. Dynamic & Adaptive to responds to real-time threats. Unpredictable & Non-Deterministic which is quantum-safe solution tailored to RTES and IoT environments.

  

This paper proposes an integrated framework that combines chaos-based encryption, true random number generation (TRNG), AI-driven anomaly detection, and post-quantum cryptographic (PQC) authentication. The proposed approach aims to provide computationally efficient encryption while ensuring adaptability to emerging cyber-security threats and long-term security against quantum adversaries for real-time embedded systems in mission-critical environments.

  

**3. Review of Literature**

  

The security challenges faced by real-time embedded systems (RTES) and IoT devices have led to extensive research into lightweight cryptography, chaos-based encryption, anomaly detection, and post-quantum cryptography. This section reviews the existing literature on these topics and identifies gaps that this research aims to address.

  

_Farah and Alshammari (2023)_ [3] propose a **hyperchaotic encryption algorithm** designed to enhance the security of image encryption systems. Their approach integrates **hyperchaotic maps with high ergodicity**, offering a significantly large **keyspace (10¹⁴ values)**, making it resistant to brute-force attacks. The encryption framework utilizes an **optimized S-box with high nonlinearity**, eliminating fixed and reverse fixed points, which strengthens resistance against differential cryptanalysis. This study highlights the potential of chaos-based cryptographic techniques in **enhancing security for multimedia transmission**, particularly in **resource-constrained environments like IoT and embedded systems**. The findings reinforce the feasibility of using **hyperchaotic encryption** in real-time security-sensitive applications.

  

_Ahvanooey et al. (2022)_ [4] provide a comprehensive review of modern authentication schemes (ASs) applicable to smartphones and IoT devices, categorizing them into text-based, graphical-based, biometrics-based, web-based, and hardware-based approaches. The study highlights that many traditional authentication mechanisms struggle with deployment in IoT environments due to hardware constraints, usability issues, and susceptibility to cyberattacks. Their empirical investigation reveals critical vulnerabilities, such as susceptibility to cracking attacks and replay attacks, which pose significant threats to IoT security. The paper also discusses mitigation strategies and proposes improvements to enhance authentication robustness.

  

_Kumar and Mishra (2022)_ [5] propose a quantum-resistant pseudo-random number generator (QRPRNG) based on the Learning with Errors (LWE) problem, a lattice-based cryptographic primitive known for its resilience against quantum attacks. Their approach integrates a Linear Feedback Shift Register (LFSR) with a homomorphic function to generate a secure and indefinite sequence of pseudo-random bits while ensuring the security of the seed. The system is subjected to NIST statistical tests, demonstrating strong randomness properties, achieving throughput of 35.172 Mbit/s.

  

_Sama et al. (2024)_ [6] introduce XORasm, a lightweight pseudo-random number generator (PRNG) designed for embedded systems such as Programmable Logic Controllers (PLCs). XORasm is based on the XORshift algorithm and utilizes a modified seed derived from the system clock to enhance randomness. The authors evaluate its statistical properties using the dieharder RNG testing suite, demonstrating that XORasm outperforms Siemens' existing 32-bit LGF_RandomRange_Dint function in terms of randomness at a 99.95% confidence level. The study highlights XORasm’s suitability for low-power embedded systems and its potential for improving cryptographic security by serving as an initialization vector for encryption schemes like AES.

  

_Onuki et al. (2022)_ [7] propose a novel method for secret-key exchange utilizing chaotic synchronization and a secure hash algorithm. Their approach integrates three chaos-based cryptographic primitives: a pseudorandom number generator (PRNG) based on the augmented Lorenz (AL) map, a secret-key exchange mechanism using synchronized randomized Lorenz oscillators, and a logistic hash function for key verification. In system, 2 legitimate users synchronize their chaotic oscillators and generate a shared binary key while preventing an eavesdropper from estimating synchronization errors due to the randomization of exchanged signals. The security of the shared key is further reinforced by verifying hash values generated through a logistic hash function, which passes the NIST SP800-22 statistical tests. The study highlights the potential of their chaos-based stream cipher in securing real-time communication, such as wireless audio and video data transmission.

  

_Dehkordi et al. (2023)_ [8] provide a comprehensive review of machine learning (ML)-based Intrusion Detection Systems (IDS) for Internet of Things (IoT) security. The study explores various IoT security threats and highlights ML classifiers, including K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Decision Tree (DT), Random Forest (RF), Naïve Bayes (NB), and Artificial Neural Networks (ANN), as effective methods for detecting cyber intrusions. The review emphasizes that hybrid classification approaches and dimensionality reduction techniques, such as Principal Component Analysis (PCA), significantly improve detection accuracy and computational efficiency. The best-performing models, including PCA-XgBoost, PCA-CatBoost, and PCA-KNN, achieved a 99.99% success rate in IDS classification. This research is relevant to adaptive security mechanisms in real-time embedded systems, as ML-driven IDS can enhance anomaly detection and threat mitigation in IoT networks. The findings align with the need for robust, scalable, and intelligent security solutions that can integrate with encryption techniques and chaos-based cryptographic methods to strengthen security in resource-constrained environments.

  

_Opiłka et al. (2024)_ [9] review the necessity of post-quantum cryptography (PQC) for digital signatures in response to the growing threats posed by quantum computing. Their literature review highlights the vulnerabilities of classical cryptographic systems, particularly RSA, under quantum attacks. The study focuses on three leading PQC algorithms—CRYSTALS-Dilithium, Falcon, and SPHINCS+—which have been shortlisted by the National Institute of Standards and Technology (NIST) for standardization. The review discusses the underlying principles of these algorithms: CRYSTALS-Dilithium: A lattice-based signature scheme known for its balance between security and performance, particularly excelling in key pair generation and signing speed. Falcon: A compact lattice-based scheme optimized for small signature sizes, making it highly efficient for bandwidth-constrained environments.

SPHINCS+: A stateless hash-based signature scheme offering high security but at the cost of larger signature sizes and slower verification times. Comparisons with traditional RSA cryptography emphasize that PQC alternatives offer significantly stronger security while maintaining acceptable efficiency trade-offs. The review also highlights ongoing NIST standardization efforts and the expectation of further optimizations in PQC algorithms.

  

**4. Research Gap**

  

While significant research has been conducted to explore chaos-based encryption, machine learning(ML)-driven anomaly detection, and post-quantum cryptography (PQC), these approaches have been largely studied in isolation. The lack of unified framework that integrates these techniques for RTES and IoT security remains unexplored and presents a critical research gap.

  

Existing chaos-based encryption methods provide high entropy and non-deterministic encryption, but do not dynamically adapt to real-time threats levels, leaving RTES vulnerable to evolving cyberattacks. Machine learning-based intrusion detection systems (IDS) have demonstrated success in identifying cyber threats but are rarely integrated with encryption mechanisms to actively modify and influence security parameters in response to detected anomalies. Existing research on post-quantum cryptography has analyzed algorithm performance, particularly in digital signatures, but its adaptation for lightweight encryption in resource-constrained RTES and IoT environments is still limited. Lattice-based PQC methods like CRYSTALS-Dilithium and Falcon offer promising security guarantees, yet their computational feasibility for embedded systems has not been extensively evaluated in conjunction with chaos-based encryption and ML-driven adaptive security.

  

Despite advancements in each individual domain, there is a lack of a cohesive security framework that leverages the strengths of chaos-based encryption, AI-driven adaptive security, and PQC authentication which is tailored for RTES and IoT applications for evolving-threats.

  

  

**5. Research Objectives**

  

The primary objective of this research is to develop a lightweight, adaptive encryption and authentication framework for real-time embedded systems (RTES) and IoT devices that enhances security while minimizing computational overhead. This study will analyse the limitations of existing cryptographic methods for encryption and authentication, particularly their computational demands, predictability and susceptibility to cyber threats. It will then explore and evaluate chaos-based encryption techniques, such as logistic maps, Lorenz attractors, and chaotic pseudo-random number generators (CPRNGs), to improve encryption unpredictability and enhance device security. Additionally, the research will integrate a machine learning-based anomaly detection model capable of real-time network monitoring to detect potential threats, and dynamically adjust encryption parameters to strengthen security and mitigate attacks in real time. The study aims to design a lightweight, adaptive security framework that incorporates true random number generation (TRNG), chaos-based cryptographic methods, and machine learning-driven security adaptation for real-time threat response. The feasibility of the proposed framework will be evaluated by comparing its security strength, computational efficiency, and adaptability against conventional encryption methods in embedded environments. Ultimately, this study seeks to contribute a novel, quantum-resistant, real-time security mechanism for embedded and IoT devices, ensuring both efficiency and resilience against evolving cyber threats.

  

**6. Proposed Methodology**

  

The proposed adaptive security framework enhances security in real-time embedded systems (RTES) and IoT devices by integrating chaos-based cryptographic key generation, AI-driven anomaly detection, and post-quantum authentication to provide adaptive and quantum-resistant security. This system is structured into three main components: a chaotic key generation and encryption mechanism for lightweight and unpredictable encryption, an AI-driven anomaly detection system for dynamic threat response, and a quantum-resistant authentication process to prevent unauthorized access and ensure future-proof security.

The **chaotic key generation and encryption mechanism** leverages the inherent unpredictability of chaotic systems, ensuring a high degree of randomness in encryption. A true random number generator (TRNG) collects entropy from physical sources such as sensor noise, electronic fluctuations, and environmental changes to generate a highly random seed.

![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_6758f94b.png)  
![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_b5adf726.png) ![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_1dea93bc.png)  

_Figure : Representation of Chaos Models_

  
  

  

This seed initializes a chaotic system—such as a logistic map, Lorenz attractor, or Chua’s circuit—to create a non-repeating, unpredictable key stream. The encryption process applies bitwise XOR operations between plaintext data and the chaotic key stream, supplemented by chaotic substitution and permutation techniques to enhance security. Due to the computational efficiency of chaotic maps, this method is well-suited for low-power RTES environments.

  

For **AI-driven anomaly detection and adaptive security**, a lightweight machine learning model continuously monitors system activity with minimal computational overhead. The model analyzes network traffic for deviations from normal behaviour, system logs for unusual activity, and power consumption patterns for potential side-channel attacks. Suitable lightweight anomaly detection techniques include autoencoders (AE) for detecting deviations from expected data patterns, long short-term memory (LSTM) models for tracking temporal anomalies, one-class support vector machines (SVM) for learning normal system behavior, and isolation forests for efficiently isolating outliers. These models are optimized for low-power devices through techniques such as pruning, quantization, and model distillation to ensure real-time intrusion detection without significant resource consumption. Upon detecting an anomaly, the system dynamically adjusts encryption parameters to counteract p![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_d439ec91.png) otential threats.

_Figure : Flowchart of Key Generation and Encryption_

  

  

  

**Adaptive responses** include reinitializing chaotic key generation with a new TRNG seed, modifying chaotic map parameters to produce a new key stream, increasing encryption complexity based on attack severity, or switching authentication methods when suspicious activity is detected. Additionally, a lightweight reinforcement learning (RL) model, such as a deep Q-network (DQN) with reduced parameters, is integrated for self-optimizing security. By analyzing past attack patterns, this model refines encryption and authentication settings over time, ensuring an optimal balance between security and computational efficiency.

![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_f971d97.png)

_Figure : AI-Driven adaptive threat response_

  

  

**Post-quantum authentication** ensures secure and tamper-proof key exchange and the identity verification is facilitated using lattice-based cryptographic methods like Kyber and NTRU, while hash-based digital signatures such as SPHINCS+ provide tamper-resistant verification without relying on traditional RSA or ECC keys. Encryption keys are derived from chaotic sequences, ensuring they are unique for each session and resistant to replay attacks. Secure key exchange is achieved through PQC-based key encapsulation mechanisms (KEMs), protecting against quantum computing threats. Additionally, the framework also incorporates session-based one-time authentication tokens enhance security by eliminating static passwords and pre-shared keys. The integration of these techniques results in a robust, adaptive, and quantum-resistant security framework designed to safeguard RTES and IoT devices against evolving cyber threats.

  

**7. Analysis and Interpretations**

  

The proposed chaos-based cryptographic approach ensures low computational overhead and unpredictability, while PQC-based authentication safeguards against both classical and quantum threats. Secure key exchange leveraging chaos theory eliminates reliance on traditional key distribution methods, enhancing resilience. AI-driven security continuously adapts to threats in real time, while reinforcement learning improves defense mechanisms over time, creating a self-optimizing security system.

  

Security strength of the proposed framework when evaluated against both classical and quantum attacks. Chaotic pseudo-random number generators (PRNGs) exhibit high entropy, non-linearity, and extreme sensitivity to initial conditions, ensuring that generated keys remain unpredictable and unique for each session. Even slight variations in input produce vastly different outputs, making cryptanalysis infeasible. Unlike traditional encryption schemes that rely on mathematical complexity and are susceptible to predictive attacks with advancing computational power, chaotic encryption dynamically evolves, making key prediction nearly impossible. No known polynomial-time algorithms exist to reverse-engineer chaotic sequences, further reinforcing security.

  

The system demonstrates strong resistance against classical attacks. In brute-force attacks, traditional encryption methods like AES-256 and RSA-4096 have predefined key search spaces, making exhaustive search attacks possible. In contrast, chaotic encryption continuously evolves, rendering brute-force attacks impractical. The framework also minimizes susceptibility to side-channel attacks by maintaining a low computational footprint, reducing power and timing signatures that adversaries can exploit. Unlike traditional key generation methods that follow predictable mathematical structures, the non-deterministic nature of chaos-based key generation prevents statistical and cryptanalysis attacks. Since chaotic encryption does not rely on frequency-based key structures, frequency analysis techniques become ineffective.

  

Regarding quantum resistance, the proposed approach does not depend on factorization or discrete logarithms, making Shor’s algorithm ineffective against it. While Grover’s algorithm can theoretically speed up key searches, chaotic encryption does not store static keys; instead, it dynamically evolves the key schedule, mitigating quantum search advantages. By incorporating post-quantum cryptographic schemes such as lattice-based and hash-based cryptography for authentication, the system eliminates dependence on RSA and ECC, ensuring long-term security in the post-quantum era.

  

A![](file:///run/user/1000/snap.libreoffice/lu3176u7l7.tmp/lu3176u7r7_tmp_d167ff02.png)  
critical factor in RTES security is computational efficiency. The proposed system is designed to impose minimal processing power, memory, and energy consumption overhead compared to RSA, ECC, and AES-based encryption. Unlike traditional encryption algorithms that involve large matrix operations and modular exponentiation, the chaotic encryption approach eliminates complex cryptographic computations, significantly reducing CPU load. Adaptive encryption strength allows dynamic trade-offs between security and performance, ensuring optimized resource utilization in constrained embedded environments.

_Figure : Processing time of classical encryption models_

  
  

Additionally, efficient key exchange through chaotic synchronization removes the need for heavy cryptographic computations, making the framework highly suitable for real-time, low-power IoT and RTES applications. Case studies show how the proposed security framework adapts to cyber threats using AI-driven anomaly detection and dynamic security adjustments. For a Man-in-the-Middle (MITM) attack, the system detects unusual packet timing and handshake patterns, then strengthens encryption by switching to a more complex chaotic function, making interception difficult. To prevent replay attacks, chaotic key generation ensures each session key is unique and unpredictable. Since chaotic systems are highly sensitive to initial conditions, even a small change creates entirely different keys, preventing reuse by attackers.

  

    
|Metric|RSA-4096|ECC-521|AES-256|Proposed Chaotic Encryption|
|---|---|---|---|---|
|Key Size (bits)|4096|521|256|128-256 (dynamic)|
|Encryption Time|High|Moderate|Low|Very Low|
|Decryption Time|High|Moderate|Low|Very Low|
|Computational Complexity|Exponential|Polynomial|Logarithmic|Logarithmic|
|Quantum Resistance|No|No|Partially|Yes|
|Adaptability|No|No|No|Yes (ML-driven)|

_Figure : Comparison of encryption metrics_

  

For AI-based intrusion detection, the system monitors network activity using an autoencoder model. If an attack pattern is detected, the model retrains itself to improve future threat detection. In response to advanced threats, the system can regenerate encryption keys, enforce multi-factor authentication, or adjust system behaviour in real-time to block attacks. This adaptive security approach ensures strong protection against evolving cyber threats.

  

**8. Limitations and Future Improvements**

  

The proposed system enhances encryption, security adaptability, and computational efficiency but faces certain limitations that must be addressed for practical implementation. Many RTES and IoT devices operate on low-power microcontrollers with limited processing capacity. Implementing chaotic key generation and AI-driven anomaly detection may require hardware accelerators or optimization techniques to ensure efficiency without excessive power consumption. While chaos-based encryption is computationally lightweight, achieving real-time performance requires careful tuning of chaotic functions. Some chaotic maps, such as the Lorenz attractor, require floating-point precision, which may not be supported on all RTES architectures, potentially limiting implementation feasibility.

  

Unlike traditional encryption, where keys are predefined, chaotic systems require sender and receiver synchronization based on shared initial conditions. Network delays, packet loss, or interference may lead to desynchronization, causing decryption failures. Although chaotic encryption minimizes computational signatures, IoT devices remain vulnerable to power analysis attacks, where attackers may infer encryption patterns from hardware power fluctuations. Attackers may also use adversarial machine learning techniques to manipulate the anomaly detection model, reducing its ability to identify cyber threats and making the system more susceptible to sophisticated attacks.

  

Several enhancements can improve the security, efficiency, and scalability of the proposed system. Implementing hardware-accelerated chaotic PRNGs and cryptographic modules can improve processing speed and power efficiency while reducing vulnerability to physical tampering and side-channel attacks. Self-recovering chaotic synchronization techniques can enhance resilience against network disruptions, ensuring continuous encryption key alignment between communicating devices. Integrating chaos-based encryption with a Zero-Trust framework ensures continuous verification of encryption keys and authentication parameters, reducing the risk of unauthorized access.

  

Reinforcement learning can enable self-healing security mechanisms, allowing systems to adapt dynamically to new cyber threats. Federated learning can facilitate decentralized threat intelligence, where multiple RTES, IoT devices collaboratively learn from distributed attack patterns without sharing sensitive data. Exploring lattice-based cryptographic signatures for RTES authentication can strengthen security against quantum computing threats, ensuring long-term resilience. The integration of chaos theory, AI-driven security, and post-quantum cryptography represents a promising direction for real-time embedded system security. Future research will be essential to translating these theoretical advancements into practical, scalable solutions for securing next-generation IoT and RTES environments.

  

**9. Conclusion**

  

This research proposed a novel security framework that combines chaos-based encryption, AI-driven anomaly detection, and post-quantum authentication to secure RTES and IoT devices. Chaos-based encryption enhances security with high-entropy, unpredictable key generation while remaining efficient for low-power devices. AI-driven anomaly detection continuously monitors network activity, adjusting encryption parameters and authentication protocols in response to potential threats. Reinforcement learning helps the system improve over time by adapting to new attack patterns. Post-quantum authentication methods, such as lattice-based and hash-based cryptography, protect devices from future quantum attacks.

The approach ensures lightweight, adaptive, and quantum-resistant security against both classical and quantum threats while remaining efficient by minimizing computational overhead. Future advancements in hardware optimization, AI adaptability, and post-quantum security will further enhance the framework’s applicability in real-world security of embedded environments.

  

**10. References**

  

[1] Seals, T. (2021, September 6). _IoT attacks skyrocket, doubling in 6 months._ Threatpost. [https://threatpost.com/iot-attacks-doubling/169224/](https://threatpost.com/iot-attacks-doubling/169224/)

**[2] Mascellino, A. (2025, February 12).** _Massive IoT data breach exposes 2.7 billion records._ **Infosecurity Magazine.** [https://www.infosecurity-magazine.com/news/iot-data-breach-exposes-27-billion/](https://www.infosecurity-magazine.com/news/iot-data-breach-exposes-27-billion/)

**[3] Farah, T., & Alshammari, B. M. (2023). A novel image encryption scheme based on a new hyperchaotic map.** _Multimedia Tools and Applications_**. Springer.** [https://doi.org/10.1007/s11042-023-16873-x](https://doi.org/10.1007/s11042-023-16873-x)

**[4] Ahvanooey, M. T., et al. (2022). Modern authentication schemes in smartphones and IoT devices: An empirical survey.** _IEEE Internet of Things Journal, 9(10)_**, 7639-7663.** [https://doi.org/10.1109/JIOT.2021.3138073](https://doi.org/10.1109/JIOT.2021.3138073)

**[5] Kumar, A., & Mishra, A. (2022). LWE-Based Quantum-Resistant Pseudo-Random Number Generator. International Arab Journal of Information Technology, 20(6).** [https://doi.org/10.34028/iajit/20/6/8](https://doi.org/10.34028/iajit/20/6/8)

**[6] Sama, A., Meyliana, Heryadi, Y., & Sahroni, T. R. (2024). Lightweight Pseudo Random Number Generator for Embedded Systems. International Journal of Safety and Security Engineering, 14(4).** [https://doi.org/10.18280/ijsse.140409](https://doi.org/10.18280/ijsse.140409)

**[7] Onuki, K., Cho, K., Horio, Y., & Miyano, T. (2022). Secret-key exchange through synchronization of randomized chaotic oscillators aided by logistic hash function. IEEE Transactions on Circuits and Systems I: Regular Papers, 69(4), 1655–1667.** [https://doi.org/10.1109/TCSI.2022.3140762](https://doi.org/10.1109/TCSI.2022.3140762)

**[8] Dehkordi, I. F., Manochehri, K., & Aghazarian, V. (2023). Internet of Things (IoT) Intrusion Detection by Machine Learning (ML): A Review. Asia-Pacific Journal of Information Technology and Multimedia, 12(1), 13–38.** [https://doi.org/10.17576/apjitm-2023-1201-02](https://doi.org/10.17576/apjitm-2023-1201-02)

**[9] Opiłka, F., Niemiec, M., Gagliardi, M., & Kourtis, M.A. (2024). Performance Analysis of Post-Quantum Cryptography Algorithms for Digital Signature. Applied Sciences, 14(12), 4994.** [https://doi.org/10.3390/app14124994](https://doi.org/10.3390/app14124994)