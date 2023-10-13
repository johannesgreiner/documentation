---
title: pauli_basis
description: API reference for qiskit.quantum_info.pauli_basis
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.quantum_info.pauli_basis
---

<span id="qiskit-quantum-info-pauli-basis" />

# qiskit.quantum\_info.pauli\_basis

<span id="qiskit.quantum_info.pauli_basis" />

`qiskit.quantum_info.pauli_basis(num_qubits, weight=False, pauli_list=None)`

Return the ordered PauliTable or PauliList for the n-qubit Pauli basis.

<Admonition title="Deprecated since version 0.22" type="danger">
  `qiskit.quantum_info.operators.symplectic.pauli_utils.pauli_basis()`’s argument `pauli_basis` is deprecated as of qiskit-terra 0.22. It will be removed no earlier than 3 months after the release date. The argument `pauli_list` has no effect as the function always returns a PauliList.
</Admonition>

**Parameters**

*   **num\_qubits** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – number of qubits
*   **weight** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – if True optionally return the basis sorted by Pauli weight rather than lexicographic order (Default: False)
*   **pauli\_list** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – \[Deprecated] This argument is deprecated and remains for backwards compatability. It has no effect.

**Returns**

the Paulis for the basis

**Return type**

[PauliList](qiskit.quantum_info.PauliList "qiskit.quantum_info.PauliList")
