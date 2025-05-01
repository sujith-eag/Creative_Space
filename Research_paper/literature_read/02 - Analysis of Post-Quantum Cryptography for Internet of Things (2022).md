

Cryptographic algorithms are crucial for secure
communication in the Internet of Things (IoT).
Quantum computers threaten public key
cryptography algorithms like RSA (Rivest,
Shamir, Adleman) and Diffie-Hellman (DH) key
exchange schemes,


solutions like Quantum Key
Distribution require heavy infrastructure. So, it
is not feasible for the Internet of Things with
fewer resources in computing power and form
factor. Post-Quantum Cryptography is helpful
on these devices. But, it needs further
developments and improvements. This paper
analyzes cryptography algorithms and protocols
of IoT with different categories. Integrated PQC
of National Institute of Standards and
Technology (NIST) third level finalists on
Raspberry Pi 4 (RPI4) board with Linux
operating system. The performance of Post-
Quantum Cryptography schemes for IoT has
been evaluated. Finally, a Post-Quantum
Cryptography scheme has been suggested for
the Internet of Things based on the performance
analysis.



Security of
the devices is less due to the low computing power,
and memory of hardware. Therefore, it is
essential to ensure confidentiality, integrity, and
authentication. The communication
between IoT nodes to gateways is to be
confidential.


Communication from IoT devices to gateway
generally includes WiFi (Wireless Fidelity) or
wired LAN (Local Area Network) connection.
Edge nodes use LoRa (Long Range), ZigBee, BLE
(Bluetooth Low Energy) protocols. These nodes
need protection from security attacks via
cryptographic algorithms. The gateway to
middleware or cloud uses internet communication
with transport layer security protocols.



uantum Key Distribution and
Post-Quantum Cryptography are the research area
to address the threats by quantum computers [10].
QKD solutions are one of the solutions and need
high infrastructure and are not feasible for desktops
and IoT nodes. So, the development and
implementation of PQC based solutions are
required. The PQC should ensure security, energy
efficiency, and lightweight on resource-constrained
devices.


we implement the quantum-safe
library from the open quantum safe (OQS) project
named liboqs on the Raspberry Pi 4 hardware
platform containing Linux operating system. The
results and trends are analyzed. Finally, we suggest
a secure and quantum-safe scheme for the Internet
of Things using PQC.



___
KEM provides a secure method to transfer
symmetric keys using quantum-safe public-key
algorithms. In this method, random number
generators generate symmetric keys:
1. The message encrypts with the generated
key
1. It transmits these keys via public key
algorithms
1. The encrypted message at the receiver
decrypts using the public-key algorithm
1. It reproduces the symmetric key




NIST Standardisation Initiatives
NIST has started the standardization of quantum-
resistant algorithms in 2017. The standardization
process moved to several rounds by publishing
finalist algorithms on each level. NIST published
security levels for PQC algorithms. It includes five
levels for ensuring the security of PQC against
classical and quantum attacks.




OQS project supports the development and
prototyping of quantum-safe cryptography. The
open-source project having a C library liboqs and
integrated PQC on OpenSSL [6], [12]. The
implementation is available on GitHub




The key generation time of
Kyber512 is less compared to other algorithms.
LightSaber-KEM took less time for encryption and
decryption.


Dilithium is a choice for
resource-constrained IoT devices.



Conclusion

PQC implementations are not available on IOT Devices.


the low-resource IoT communications can use LightSaber-KEM and Dilithium2 algorithms for quantum resistance. The
LightSaber-KEM and Dilithium2 algorithms will
preserve the life of battery power and execution time