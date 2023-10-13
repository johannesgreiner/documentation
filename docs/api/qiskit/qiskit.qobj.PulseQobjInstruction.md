---
title: PulseQobjInstruction
description: API reference for qiskit.qobj.PulseQobjInstruction
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.qobj.PulseQobjInstruction
---

# PulseQobjInstruction

<span id="qiskit.qobj.PulseQobjInstruction" />

`qiskit.qobj.PulseQobjInstruction(name, t0, ch=None, conditional=None, val=None, phase=None, duration=None, qubits=None, memory_slot=None, register_slot=None, kernels=None, discriminators=None, label=None, type=None, pulse_shape=None, parameters=None, frequency=None)`

Bases: [`object`](https://docs.python.org/3/library/functions.html#object "(in Python v3.11)")

A class representing a single instruction in an PulseQobj Experiment.

Instantiate a new PulseQobjInstruction object.

**Parameters**

*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – The name of the instruction
*   **t0** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – Pulse start time in integer **dt** units.
*   **ch** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – The channel to apply the pulse instruction.
*   **conditional** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – The register to use for a conditional for this instruction
*   **val** ([*complex*](https://docs.python.org/3/library/functions.html#complex "(in Python v3.11)")) – Complex value to apply, bounded by an absolute value of 1.
*   **phase** ([*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")) – if a `fc` instruction, the frame change phase in radians.
*   **frequency** ([*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")) – if a `sf` instruction, the frequency in Hz.
*   **duration** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – The duration of the pulse in **dt** units.
*   **qubits** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – A list of `int` representing the qubits the instruction operates on
*   **memory\_slot** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – If a `measure` instruction this is a list of `int` containing the list of memory slots to store the measurement results in (must be the same length as qubits). If a `bfunc` instruction this is a single `int` of the memory slot to store the boolean function result in.
*   **register\_slot** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – If a `measure` instruction this is a list of `int` containing the list of register slots in which to store the measurement results (must be the same length as qubits). If a `bfunc` instruction this is a single `int` of the register slot in which to store the result.
*   **kernels** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – List of [`QobjMeasurementOption`](qiskit.qobj.QobjMeasurementOption "qiskit.qobj.QobjMeasurementOption") objects defining the measurement kernels and set of parameters if the measurement level is 1 or 2. Only used for `acquire` instructions.
*   **discriminators** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – A list of [`QobjMeasurementOption`](qiskit.qobj.QobjMeasurementOption "qiskit.qobj.QobjMeasurementOption") used to set the discriminators to be used if the measurement level is 2. Only used for `acquire` instructions.
*   **label** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – Label of instruction
*   **type** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – Type of instruction
*   **pulse\_shape** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – The shape of the parametric pulse
*   **parameters** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – The parameters for a parametric pulse

## Methods

### from\_dict

<span id="qiskit.qobj.PulseQobjInstruction.from_dict" />

`classmethod from_dict(data)`

Create a new PulseQobjExperimentConfig object from a dictionary.

**Parameters**

**data** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – A dictionary for the experiment config

**Returns**

The object from the input dictionary.

**Return type**

[PulseQobjInstruction](#qiskit.qobj.PulseQobjInstruction "qiskit.qobj.PulseQobjInstruction")

### to\_dict

<span id="qiskit.qobj.PulseQobjInstruction.to_dict" />

`to_dict()`

Return a dictionary format representation of the Instruction.

**Returns**

The dictionary form of the PulseQobjInstruction.

**Return type**

[dict](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")
