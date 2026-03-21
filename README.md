# [[5,1,3]] Quantum Error Correction Code

A Qiskit implementation of the 5-qubit quantum error-correcting code, the smallest code that can correct any single-qubit error.

The [[5,1,3]] code encodes 1 logical qubit into 5 physical qubits with code distance 3. It is called *perfect* because it saturates the quantum Hamming bound — all 15 nonzero 4-bit syndromes map to distinct correctable errors with none left over. Syndrome extraction uses ancilla qubits and phase kickback to measure the stabilizer generators without disturbing the encoded state, and classical feedforward applies the appropriate correction based on the result.

The notebook derives everything from first principles: the stabilizer group, logical codewords, syndrome lookup table, and circuit construction. It then verifies correctness across all single-qubit error cases and simulates logical success rate under depolarizing noise at varying physical error rates.

## Usage

Open `513qec_code.ipynb` and run all cells. Dependencies are installed in the first cell.

## Relevant Papers
- C.H. Bennett, D.P. DiVincenzo, J.A. Smolin, W.K. Wootters, “Mixed State Entanglement and Quantum Error Correction”, Phys. Rev. A. 54 (5), 3824-3851 (1996). [[arXiv:quant-ph/9604024]](https://arxiv.org/abs/quant-ph/9604024)
- D. Gottesman, "Stabilizer Codes and Quantum Error Correction", Caltech Ph.D. Thesis (1997). [[arXiv:quant-ph/9705052]](https://arxiv.org/abs/quant-ph/9705052)
- R. Laflamme, C. Miquel, J.P. Paz, W.H. Zurek, "Perfect Quantum Error Correction Code", Phys. Rev. Lett. 77, 198-201 (1996). [[arXiv:quant-ph/9602019]](https://arxiv.org/abs/quant-ph/9602019)

## Links
- "Five-qubit error correcting code", [[Wikipedia]](https://en.wikipedia.org/wiki/Five-qubit_error_correcting_code)
- [Qiskit Documentation](https://docs.quantum.ibm.com/)
