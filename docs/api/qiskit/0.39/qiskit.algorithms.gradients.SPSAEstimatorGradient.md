---
title: SPSAEstimatorGradient
description: API reference for qiskit.algorithms.gradients.SPSAEstimatorGradient
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.algorithms.gradients.SPSAEstimatorGradient
---

# SPSAEstimatorGradient

<span id="qiskit.algorithms.gradients.SPSAEstimatorGradient" />

`SPSAEstimatorGradient(estimator, epsilon, batch_size=1, seed=None, **options)`

Bases: [`qiskit.algorithms.gradients.base_estimator_gradient.BaseEstimatorGradient`](qiskit.algorithms.gradients.BaseEstimatorGradient "qiskit.algorithms.gradients.base_estimator_gradient.BaseEstimatorGradient")

Compute the gradients of the expectation value by the Simultaneous Perturbation Stochastic Approximation (SPSA).

**Parameters**

*   **estimator** ([*BaseEstimator*](qiskit.primitives.BaseEstimator "qiskit.primitives.BaseEstimator")) – The estimator used to compute the gradients.
*   **epsilon** (*float*) – The offset size for the SPSA gradients.
*   **batch\_size** (*int*) – The number of gradients to average.
*   **seed** (*int | None*) – The seed for a random perturbation vector.
*   **options** – Primitive backend runtime options used for circuit execution. The order of priority is: options in `run` method > gradient’s default options > primitive’s default setting. Higher priority setting overrides lower priority setting

**Raises**

**ValueError** – If `epsilon` is not positive.

## Methods

### run

<span id="qiskit.algorithms.gradients.SPSAEstimatorGradient.run" />

`SPSAEstimatorGradient.run(circuits, observables, parameter_values, parameters=None, **options)`

Run the job of the estimator gradient on the given circuits.

**Parameters**

*   **circuits** – The list of quantum circuits to compute the gradients.
*   **observables** – The list of observables.
*   **parameter\_values** – The list of parameter values to be bound to the circuit.
*   **parameters** – The sequence of parameters to calculate only the gradients of the specified parameters. Each sequence of parameters corresponds to a circuit in `circuits`. Defaults to None, which means that the gradients of all parameters in each circuit are calculated.
*   **options** – Primitive backend runtime options used for circuit execution. The order of priority is: options in `run` method > gradient’s default options > primitive’s default setting. Higher priority setting overrides lower priority setting

**Returns**

The job object of the gradients of the expectation values. The i-th result corresponds to `circuits[i]` evaluated with parameters bound as `parameter_values[i]`. The j-th element of the i-th result corresponds to the gradient of the i-th circuit with respect to the j-th parameter.

**Raises**

**ValueError** – Invalid arguments are given.

### update\_default\_options

<span id="qiskit.algorithms.gradients.SPSAEstimatorGradient.update_default_options" />

`SPSAEstimatorGradient.update_default_options(**options)`

Update the gradient’s default options setting.

**Parameters**

**\*\*options** – The fields to update the default options.

## Attributes

<span id="qiskit.algorithms.gradients.SPSAEstimatorGradient.options" />

### options

Return the union of estimator options setting and gradient default options, where, if the same field is set in both, the gradient’s default options override the primitive’s default setting.

**Return type**

[`Options`](qiskit.providers.Options "qiskit.providers.options.Options")

**Returns**

The gradient default + estimator options.
