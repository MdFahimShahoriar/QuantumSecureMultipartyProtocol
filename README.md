
# **Secured Quantum Multiparty Communication Protocol for Imperfect Channels Utilizing W-States**

## **Overview**
This project presents a secure multiparty communication protocol leveraging the W-state entanglement in quantum communication to overcome challenges in imperfect channels. The protocol ensures secure key distribution, message encryption, and eavesdropping detection. The integration of a third-party mediator ("Charlie") and decoy photons enhances security, making the system more resilient to noise and external attacks.

## **Features**
- **Quantum Key Distribution (QKD):** Secure key sharing using entangled W-states.
- **Noise Resilience:** Improved tolerance to communication channel imperfections.
- **Eavesdropping Detection:** Integration of decoy photons and statistical analysis to detect intrusions.
- **Multiparty Communication:** Secure and selective message transmission between multiple parties.
- **Third-Party Monitoring:** Charlie acts as a neutral mediator for system integrity.
- **Encryption Security:** AES-128 encryption with SHA-256 hashing.


## **Workflow**

1. **W-State Generation:**  
   A quantum circuit generates W-states using IBM's Qiskit library.  
   
2. **Key Distribution:**  
   - Alice, Bob, and David measure entangled qubits using Z-basis to generate shared secret keys.
   - Charlie anonymously validates key integrity and detects entanglement discrepancies.

3. **Message Encryption & Transmission:**  
   - Alice encrypts messages using AES-128 and transmits them selectively to Bob and/or David using unique tokens.
   - Decoy photons detect eavesdropping by monitoring for disturbances in communication.

4. **Eavesdropping Detection:**  
   - Charlie analyzes entanglement states and decoy photon discrepancies.
   - Quantum Bit Error Rate (QBER) assessment differentiates noise from security threats.

5. **Security Analysis:**  
   - Resistance to direct measurement and ancilla particle attacks.
   - Evaluation of protocol performance under noise conditions.


## **Project Structure**


📂 SecuredQuantumMultipartyProtocol  
├── 📁 circuits/               # Quantum circuits for W-state generation  
├── 📁 encryption/             # AES-128 encryption and key generation scripts  
├── 📁 simulation_results/     # Noise analysis and security evaluation reports  
├── 📁 eavesdropping_detection # Decoy photon detection and QBER assessment  
└── README.md                  # Project documentation  



## **Setup and Installation**

1. **Clone the Repository:**  
   ```bash
   git clone https://github.com/YourUsername/SecuredQuantumMultipartyProtocol.git
   cd SecuredQuantumMultipartyProtocol
 
2. **Install Dependencies:**  
   Ensure you have Python 3.x and the following packages installed:  
   ```bash
   pip install qiskit numpy cryptography matplotlib
   ```

---

## **Running the Project**

1. **Simulate W-State Generation:**  
   Execute the circuit simulation:
   ```bash
   python circuits/w_state_generation.py
   ```

2. **Perform Key Distribution:**  
   ```bash
   python key_distribution.py
   ```

3. **Run Eavesdropping Detection:**  
   ```bash
   python eavesdrop_detection.py
   ```

4. **Analyze Noise Effects:**  
   ```bash
   python noise_analysis.py
   ```

---

## **Results**
- **Noise Analysis:** The protocol shows high resilience to bit-flip and phase-flip noise, with a gradual decline in success probability under depolarizing noise.
- **Eavesdropping Detection:** Decoy photon monitoring effectively identifies unauthorized access attempts.
- **Selective Communication:** Successful encryption and decryption demonstrate secure and flexible message transmission.

---

## **Key Findings**
- **Improved Security:** The protocol effectively resists external attacks and detects eavesdropping using Charlie and decoy photons.
- **High Noise Tolerance:** W-states provide greater resilience compared to GHZ states in noisy environments.
- **Efficient Communication:** Secure multiparty message transmission is achieved without compromising speed or integrity.

---

## **Future Work**
- Integrate dynamic key distribution for real-time applications.
- Expand protocol scalability for large quantum communication networks.
- Implement additional attack detection mechanisms.

---

## **Contributors**
- Md. Rayhan Kabir Khan  
- Md. Fahim Shahoriar Titu  
- M.R.C. Mahdy  

---

## **License**
This project is licensed under the [MIT License](LICENSE).

---

## **Acknowledgments**
This project was supported by the Department of Electrical and Computer Engineering at North South University. The IBM Quantum platform was instrumental in simulating the W-state circuits and security assessments.
```  
