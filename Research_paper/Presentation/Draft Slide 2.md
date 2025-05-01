
### Introduction: Security Challenges in Embedded Systems & IoT

- Growth of IoT & RTES : Revolutionizing industries (healthcare, infrastructure, consumer) through real-time automation & connectivity.

- Vulnerabilities :  IoT devices face risks due to always-on connectivity, weak authentication, and poor security updates.

- Security Challenges :  Cyber-attacks thrive on IoT’s low power, limited resources, and weak security provisions.  Vulnerabilities lead to data theft, botnets, and cryptocurrency mining.

- Traditional Encryption Limitations :  RSA, AES, ECC unsuitable for IoT due to high computational cost & quantum threats.

- Authentication Issues : MITM attacks, replay attacks, and firmware tampering arise due to weak cryptographic implementations.

- Real-world Impact : Hacked devices can lead to severe consequences in critical sectors (healthcare, transportation, automation).

- Need for Advanced Security : Need for lightweight, efficient, adaptive encryption with long-term quantum resilient solutions tailored for IoT & RTES. 


---

**Proposed Solution:**

- **Integrated Framework** combining:    
    - Chaos-based encryption
    - True Random Number Generation (TRNG)
    - AI-driven anomaly detection
    - Post-Quantum Cryptographic (PQC) authentication

### Literature Review: Key Contributions

1. Farah & Alshammari (2023)    
    - Proposed **hyperchaotic encryption** for image security in IoT. Large keyspace (10¹⁴ values), optimized S-box for resistance to differential cryptanalysis.
    - **Impact:** Enhances security in resource-constrained systems like IoT.

2. **Ahvanooey et al. (2022)**
    - Reviewed **authentication schemes** for IoT and Highlighted vulnerabilities: cracking & replay attacks.
    
3. **Kumar & Mishra (2022)**
    - Proposed **quantum-resistant pseudo-random number generator (QRPRNG)** using LWE problem.
    - **Key Feature:** LFSR-based approach, strong randomness, and NIST compliance.
    
4. **Sama et al. (2024)**    
    - Introduced **XORasm**, a lightweight PRNG for embedded systems which Outperforms Siemens' existing random number generation.

5. **Onuki et al. (2022)**    
    - Developed **chaotic synchronization** for secret-key exchange. Secure key generation via synchronized chaotic oscillators.
    - **Impact:** Secures real-time communication (e.g., wireless data transmission).
 
6. **Dehkordi et al. (2023)**    
    - Reviewed **ML-based Intrusion Detection Systems (IDS)** for IoT. Highlighted top-performing models: PCA-XgBoost, PCA-KNN with 99.99% success rate.

7. **Opiłka et al. (2024)**    
    - Reviewed **Post-Quantum Cryptography (PQC)** for digital signatures.
    - **Key Algorithms:** CRYSTALS-Dilithium, Falcon, SPHINCS+ (NIST contenders).

---
