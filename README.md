# Differential Fault Analysis (DFA) on AES-128 : Dawn of Traditional Encryption
## Overview:
This project demonstrates the use of Differential Fault Analysis (DFA) on the AES (Advanced Encryption Standard) algorithm to perform cryptanalysis by exploiting faults injected into specific rounds of the encryption process. The primary goal is to retrieve key hypotheses by comparing correct ciphertexts with faulty ciphertexts, derived through the application of various DFA techniques. This is done over multiple phases using matrices representing the AES input and corresponding faulty ciphertexts.

Project Structure
The project is divided into the following main sections:

AES Encryption and Faulty Encryption Functions:

Functions for AES encryption and the simulation of faulty encryption by modifying specific rounds are defined.
DFA Phase 1:

Phase 1 of the DFA applies differential relations (delta relations) on the ciphertexts obtained from both the correct and faulty AES encryptions. This is used to narrow down possible key hypotheses for each key column in the AES key schedule.
DFA Phase 2:

Phase 2 uses the hypotheses generated in Phase 1 and applies further conditions (e.g., f_1, f_2) to narrow down the subkey guesses. This phase iterates through the hypotheses and refines them by testing the relations with the faulty ciphertexts.
Key Hypothesis Intersection:

The project includes a function that intersects key hypotheses from different sets of ciphertexts, refining the key guesses further.
Example Matrices:

Example matrices (Matrix2, Matrix3, etc.) are provided to test the code. These matrices represent plaintext inputs for the AES algorithm, and some are modified for simulating faults.
Output:

The code outputs possible key subkeys for each column, printing the results for each hypothesis phase, and shows the intersection of key hypotheses for further refinement.
Features
DFA on AES: The code applies Differential Fault Analysis to narrow down the key space for AES encryption.
Support for Multiple Phases: The analysis includes multiple phases of DFA, such as Phase 1 for delta relations and Phase 2 for further key refinement using conditions like f_1, f_2, and f_11.
Intersection of Hypotheses: The project provides functionality to intersect key hypotheses obtained from multiple rounds, which helps in identifying the correct key subkeys.
Fault Injection: The code simulates faults during encryption, allowing for the generation of faulty ciphertexts to be used in the analysis.
Usage
Requirements
Python 3.x
Required libraries: time (Standard Library), numpy (for matrix operations), sympy (optional, for symbolic operations or extended computations)
Instructions
Encrypt with AES:

encrypt function is used to perform encryption on the given plaintext matrix using a specified AES key.
Fault Injection:

The faulty_encrypt_on_round8 function injects faults at the 8th round of AES encryption.
DFA Analysis:

DFA8_phase1: This function is used to apply the delta relations for Phase 1 of DFA, taking in the correct and faulty ciphertexts to generate key hypotheses for each AES key column.
DFA8_phase2: This function further refines the key hypotheses by applying conditions like f_1 and f_2.
Intersection of Key Hypotheses:

The intersect_key_hypotheses function takes two sets of key hypotheses and finds the intersection, reducing the key space
