# Quantum Computing and Cryptography

Ideas on Quantum Computing, Cryptography and Communication Algorithms.

Powered by Google Cirq and Python.

![image](https://github.com/user-attachments/assets/d9feaed5-cd4c-4725-8c11-1f7a60b5dbcc)

## Is Faster-than-Light Quantum Communication Possible?

According to bibliography Quantum Communication is impossible with information rate larger than a classical channel: *Quantum Information, Computation and cryptography, Benatti, Fannes, Floreanini, Petritis: pp 210 - theorem HSV and Lemma 1*

Also, this problem is related to time-travel because if you can send information faster than light you possible can send it also to the past or future. Read: https://www.newscientist.com/article/mg26234932-900-quantum-time-travel-the-experiment-to-send-a-particle-into-the-past/ (full version https://shorturl.at/0HIAF)

Gedankenexperimenten here too: *Nonclassical Advantage in Metrology Established via Quantum Simulations of Hypothetical Closed Timelike Curves* https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.131.150202

- Our protocols prepare 1000 entangled qubit pairs that are separated and sent to 2 locations (L1 and L2).
- We want to sent two classical bits `b1` and `b2` from L1 to L2.
- But we send only another bit `b3` using the quantum protocol for location L1.
- Can the operator of the quantum protocol for location L2 decode the original two bits `b1` and `b2`?
- You can repeat this protocol to estimate the success rate... (larger than 50% success rate is good)


### Failed Attemp #1: What is the best threshold? <img width="995" alt="image" src="https://github.com/user-attachments/assets/6ee7069b-2e97-4e61-a83e-313a396baa29">
```
Best threshold: 0.8540
Best success rate: 0.3100
```
### Failed Attemp #2
```bash
Number of runs: 1000
Success rate: 0.2440
Error rate: 0.7560
```
### Failed Attempt #3
```
Number of runs: 1000
Overall success rate: 0.5230
Success rate for b1: 0.5240
Success rate for b2: 0.5300
Overall error rate: 0.4770
---
Number of runs: 10000
Overall success rate: 0.5054
Success rate for b1: 0.5099
Success rate for b2: 0.5096
Overall error rate: 0.4946
---
Number of runs: 1000 (2000 qubit pairs)
Overall success rate: 0.5120
Success rate for b1: 0.5130
Success rate for b2: 0.5120
Overall error rate: 0.4880
---
Number of runs: 1000 (4000 qubit paris per run)
Overall success rate: 0.5060
Success rate for b1: 0.5060
Success rate for b2: 0.5060
Overall error rate: 0.4940
---
Number of runs: 1000 (500 qubit pairs)
Overall success rate: 0.4690
Success rate for b1: 0.4870
Success rate for b2: 0.4910
Overall error rate: 0.5310
```
