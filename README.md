# Differential Fault Analysis (DFA) on AES-128 : Dawn of Traditional Encryption
## Overview:
This project demonstrates the use of Differential Fault Analysis (DFA) on the AES (Advanced Encryption Standard) algorithm to perform cryptanalysis by exploiting faults injected into specific rounds of the encryption process. The primary goal is to retrieve key hypotheses by comparing correct ciphertexts with faulty ciphertexts, derived through the application of various DFA techniques. This is done over multiple phases using matrices representing the AES input and corresponding faulty ciphertexts.

Project Structure
The project is divided into the following main sections:

AES Encryption and Faulty Encryption Functions:

Functions for AES encryption and the simulation of faulty encryption by modifying specific rounds are defined.
### DFA Phase 1:

Phase 1 of the DFA applies differential relations (delta relations) on the ciphertexts obtained from both the correct and faulty AES encryptions. This is used to narrow down possible key hypotheses for each key column in the AES key schedule.

### DFA Phase 2:

Phase 2 uses the hypotheses generated in Phase 1 and applies further conditions (e.g., f_1, f_2) to narrow down the subkey guesses. This phase iterates through the hypotheses and refines them by testing the relations with the faulty ciphertexts.
