# Quill ⚛️

**A quantum computing playground for learning through text.**

Quill explores quantum computing through a simple idea: what if we learned quantum states, gates, superposition, and entanglement using characters and strings instead of only abstract qubits?

The project introduces two abstractions:

- **Knot** — an eight-qubit register encoding a character.
- **Cord** — an ordered composition of Knots representing a string.

Built with Python and Qiskit, Quill is an educational playground for exploring how quantum operations affect encoded text, how measurements produce classical outcomes, and how reversible string predicates can connect to quantum search.

> **Status:** Educational prototype. The notebooks are an evolving exploration of quantum computing concepts.

---

## The idea

In the current ASCII implementation, each character is represented by an eight-qubit register. A string is represented by composing these registers in order.

For example, the Cord `HI` is represented as:

```math
|\mathrm{HI}\rangle_C
=
|H\rangle_K \otimes |I\rangle_K
```

Here, \(K\) labels a Knot and \(C\) labels a Cord. The tensor product denotes the joint state of the two character registers.

A Knot is a register, not necessarily an entangled state. Likewise, composing Knots into a Cord does not automatically entangle them.

### What happens when we apply a gate?

Quantum gates act on the underlying quantum state—not on the semantic meaning of a character.

For example, the ASCII values of `H` and `I` are 72 and 73. In binary:

```math
H = 01001000
```

```math
I = 01001001
```

They differ by one bit. Applying an X gate to the corresponding least-significant qubit transforms the encoded basis state for `H` into the basis state for `I`.

The character change is a consequence of the encoding, not a property understood by the gate.

---

## Learning path

The notebooks progress from basic character encoding to quantum search.

| Notebook | Topic | What you'll explore |
|---|---|---|
| [01 — Cord Notation & Encoding](01_cord_notation_and_encoding.ipynb) | Encoding | Represent characters and strings as quantum registers. |
| [02 — Transforming Knots with Gates](02_transforming_knots_with_gates.ipynb) | Quantum gates | Apply X gates, derive state changes, and decode measurements. |
| [03 — Hadamard & Rotation Gates](03_hadamard_and_rotation_gates.ipynb) | Superposition | Explore probabilistic measurement outcomes and rotations. |
| [04 — Entangled Knots](04_entangled_knots.ipynb) | Entanglement | Study correlations between qubits in different character registers. |
| [05 — Controlled Operations](05_controlled_operations_between_knots.ipynb) | Control | Use one qubit to control an operation on another. |
| [06 — Quantum Interference](06_quantum_interference.ipynb) | Interference | Explore how probability amplitudes reinforce or cancel. |
| [07 — String Predicates](07_string_predicates.ipynb) | Reversible computation | Build circuits that evaluate conditions on encoded strings. |
| [08 — Phase Oracles & Quantum String Search](08_phase_oracles_and_quantum_string_search.ipynb) | Quantum search | Explore phase marking and Grover's algorithm. |
| [09 — Quill Capstone](09_quill_capstone_end_to_end.ipynb) | Integration | Bring encoding, gates, entanglement, and measurement together. |

Each notebook includes mathematical explanations, circuit experiments, and exercises to encourage learning by doing.

---

## Getting started

### Option 1: Google Colab

The easiest way to get started is to open a notebook in Google Colab.

1. Clone or download this repository.
2. Upload a notebook to [Google Colab](https://colab.research.google.com/), or open it from a GitHub URL.
3. Install any dependencies specified in the notebook.
4. Run the cells sequentially and experiment with the circuits.

### Option 2: Run locally

Clone the repository:

```bash
git clone https://github.com/mohamedAkif/Quill.git
cd Quill
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```powershell
.venv\Scripts\activate
```

Install the dependencies required