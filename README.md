\# Quill



\*\*A quantum computing playground for learning through text.\*\*



Quill explores quantum computing by representing characters as quantum registers and strings as ordered compositions of those registers.



\## Learning path



1\. \*\*Cord Notation \& Encoding\*\* — Encode characters using qubits.

2\. \*\*Transforming Knots with Gates\*\* — Explore X gates and character changes.

3\. \*\*Hadamard \& Rotation Gates\*\* — Create superposition and probabilistic outcomes.

4\. \*\*Entangled Knots\*\* — Study correlations between quantum registers.

5\. \*\*Controlled Operations\*\* — Use one qubit to control another.

6\. \*\*Quantum Interference\*\* — Explore amplitude reinforcement and cancellation.

7\. \*\*String Predicates\*\* — Build reversible circuits that test string properties.

8\. \*\*Phase Oracles \& Quantum String Search\*\* — Explore phase marking and Grover's algorithm.

9\. \*\*Quill Capstone\*\* — Combine the concepts in an end-to-end experiment.



\## Core notation



A character is represented by an eight-qubit register in the current ASCII implementation.



For example, a two-character Cord can be represented as



$$

|\\mathrm{HI}\\rangle\_C

=

|H\\rangle\_K \\otimes |I\\rangle\_K

$$



where $K$ denotes a Knot and $C$ denotes a Cord.



\## Getting started



These notebooks are designed for Google Colab or a local Jupyter environment.



Install the required dependencies before running the notebooks.



\## Scope



Quill is an educational project. Encoding text in quantum states does not, by itself, provide a quantum speedup.

