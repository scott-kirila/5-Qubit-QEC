# [[5,1,3]] Quantum Error Correction Code

A Qiskit implementation of the 5-qubit quantum error-correcting code, the smallest code that can correct any single-qubit error.

The [[5,1,3]] code encodes 1 logical qubit into 5 physical qubits with code distance 3. It is called *perfect* because it saturates the quantum Hamming bound — all 15 nonzero 4-bit syndromes map to distinct correctable errors with none left over. Syndrome extraction uses ancilla qubits and phase kickback to measure the stabilizer generators without disturbing the encoded state, and classical feedforward applies the appropriate correction based on the result.

The notebook derives everything from first principles: the stabilizer group, logical codewords, syndrome lookup table, and circuit construction. It then verifies correctness across all single-qubit error cases and simulates logical success rate under depolarizing noise at varying physical error rates.

## Usage

Open `513qec_code.ipynb` and run all cells. Dependencies are installed in the first cell.
