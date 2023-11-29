<span id="qiskit-qobj-qobjexperimentheader" />

# qiskit.qobj.QobjExperimentHeader

<span id="undefined" />

`QobjExperimentHeader(**kwargs)`

A class representing a header dictionary for a Qobj Experiment.

Instantiate a new Qobj dict field object.

**Parameters**

**kwargs** – arbitrary keyword arguments that can be accessed as attributes of the object.

<span id="undefined" />

`__init__(**kwargs)`

Instantiate a new Qobj dict field object.

**Parameters**

**kwargs** – arbitrary keyword arguments that can be accessed as attributes of the object.

## Methods

|                                                                                                                  |                                                             |
| ---------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [`__init__`](#qiskit.qobj.QobjExperimentHeader.__init__ "qiskit.qobj.QobjExperimentHeader.__init__")(\*\*kwargs) | Instantiate a new Qobj dict field object.                   |
| [`from_dict`](#qiskit.qobj.QobjExperimentHeader.from_dict "qiskit.qobj.QobjExperimentHeader.from_dict")(data)    | Create a new QobjHeader object from a dictionary.           |
| [`to_dict`](#qiskit.qobj.QobjExperimentHeader.to_dict "qiskit.qobj.QobjExperimentHeader.to_dict")()              | Return a dictionary format representation of the QASM Qobj. |

<span id="undefined" />

`classmethod from_dict(data)`

Create a new QobjHeader object from a dictionary.

**Parameters**

**data** (*dict*) – A dictionary representing the QobjHeader to create. It will be in the same format as output by [`to_dict()`](#qiskit.qobj.QobjExperimentHeader.to_dict "qiskit.qobj.QobjExperimentHeader.to_dict").

**Returns**

The QobjDictField from the input dictionary.

**Return type**

QobjDictFieldr

<span id="undefined" />

`to_dict()`

Return a dictionary format representation of the QASM Qobj.

**Returns**

The dictionary form of the QobjHeader.

**Return type**

dict