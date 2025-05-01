
The security challenges faced by **real-time embedded systems (RTES) and IoT devices** have led to extensive research into **lightweight cryptography, chaos-based encryption, anomaly detection, and post-quantum cryptography**. This section reviews the existing literature on these topics and identifies gaps that this research aims to address.

## **1. Security Challenges in RTES and IoT Devices**

Real-time embedded systems and IoT devices are increasingly deployed in **critical sectors** such as healthcare, industrial automation, and smart infrastructure. However, their **low computational power, always-on connectivity, and limited security provisions** make them **highly vulnerable to cyberattacks**.

- IoT-based attacks have increased **by 400% since 2019**, with major threats including **DDoS attacks, firmware manipulation, and unauthorized access**. {link}
- Traditional security models rely on **predefined encryption schemes** that do not adapt dynamically to real-time threats, making them vulnerable to **zero-day exploits**. {link}
- Authentication in RTES is often **static and predictable**, allowing attackers to bypass weak identity verification mechanisms using **replay attacks and MITM attacks**.

## **2. Limitations of Traditional Cryptographic Techniques**

Existing encryption methods, such as **RSA, ECC, and AES**, rely on **deterministic mathematical problems**, such as prime factorization and elliptic curve calculations, for security. While these methods are robust today, research warns that:

- **Quantum computers** will eventually break RSA and ECC encryption using **Shor’s algorithm**, making them obsolete. {link}
- **Computational complexity** in asymmetric encryption leads to **high power consumption**, making it unsuitable for resource-constrained RTES. {link}
- Traditional cryptography lacks **dynamic adaptation**, meaning it does not adjust to **real-time security threats**.

## **3. Chaos-Based Cryptography for Unpredictability**

Chaotic systems, such as **logistic maps, Lorenz attractors, and Chua’s circuits**, exhibit **high sensitivity to initial conditions**, making them excellent candidates for **pseudo-random number generation (PRNG)** in cryptographic applications. Research has demonstrated that:

- **Chaos-based encryption algorithms** can generate **high-entropy keys** that are computationally infeasible to predict. {link}
- Chaotic systems offer **lower computational cost** compared to RSA and ECC while maintaining high security.{link}
- The **3D chaotic attractor models** have been successfully used for **image encryption and secure communications**, proving their feasibility in embedded applications. {link}


## **4. Machine Learning-Based Anomaly Detection for Security**

AI and ML techniques have been widely studied for **intrusion detection** and **network anomaly detection**, showing significant improvements in identifying cyber threats in real-time. Research highlights that:

- **Deep learning models** (CNNs, RNNs) can accurately detect **malicious traffic** in IoT networks. {link}
- **Unsupervised learning techniques**, such as autoencoders and clustering algorithms, can identify **previously unknown attack patterns**. {link}
- Integrating **ML with cryptographic security mechanisms** has been proposed to dynamically **adjust encryption parameters based on detected anomalies**. {link}

## **5. Post-Quantum Cryptography (PQC) and Future-Proof Security**

To address the **threat of quantum computing**, researchers have proposed **post-quantum cryptographic (PQC) algorithms**, such as:

- **Lattice-based encryption (NTRU, Kyber)** – Resistant to Shor’s algorithm and suitable for constrained devices.
- **Hash-based signatures (SPHINCS+)** – Provide quantum-resistant authentication with lightweight implementations.
- **Code-based cryptography (McEliece algorithm)** – Offers long-term security but requires large key sizes.

