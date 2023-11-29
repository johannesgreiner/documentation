---
title: AerJob
description: API reference for qiskit_aer.jobs.AerJob
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit_aer.jobs.AerJob
---

# AerJob[¶](#aerjob "Permalink to this headline")

<span id="qiskit_aer.jobs.AerJob" />

`AerJob(backend, job_id, fn, qobj=None, circuits=None, noise_model=None, config=None, executor=None)`

Bases: [`qiskit.providers.job.JobV1`](qiskit.providers.JobV1 "qiskit.providers.job.JobV1")

AerJob class for Qiskit Aer Simulators.

Initializes the asynchronous job.

**Parameters**

*   **backend** (*AerBackend*) – the backend used to run the job.
*   **job\_id** (*str*) – a unique id in the context of the backend used to run the job.
*   **fn** (*function*) – a callable function to execute qobj on backend. This should usually be a bound `AerBackend._run()` method, with the signature (qobj: QasmQobj, job\_id: str) -> Result.
*   **qobj** ([*QasmQobj*](qiskit.qobj.QasmQobj "qiskit.qobj.QasmQobj")) – qobj to execute
*   **circuits** (*list of QuantumCircuit*) – circuits to execute. If qobj is set, this argument is ignored.
*   **noise\_model** ([*NoiseModel*](qiskit_aer.noise.NoiseModel "qiskit_aer.noise.NoiseModel")) – noise\_model to execute. If qobj is set, this argument is ignored.
*   **config** (*dict*) – configuration to execute. If qobj is set, this argument is ignored.
*   **executor** (*ThreadPoolExecutor or dask.distributed.client*) – The executor to be used to submit the job.

**Raises**

[**JobError**](qiskit.providers.JobError "qiskit.providers.JobError") – if no qobj and no circuits.

## Methods

### backend

<span id="qiskit_aer.jobs.AerJob.backend" />

`AerJob.backend()`

Return the instance of the backend used for this job.

### cancel

<span id="qiskit_aer.jobs.AerJob.cancel" />

`AerJob.cancel()`

Attempt to cancel the job.

### cancelled

<span id="qiskit_aer.jobs.AerJob.cancelled" />

`AerJob.cancelled()`

Return whether the job has been cancelled.

**Return type**

`bool`

### circuits

<span id="qiskit_aer.jobs.AerJob.circuits" />

`AerJob.circuits()`

Return the list of QuantumCircuit submitted for this job.

**Returns**

the list of QuantumCircuit submitted for this job.

**Return type**

list of QuantumCircuit

### done

<span id="qiskit_aer.jobs.AerJob.done" />

`AerJob.done()`

Return whether the job has successfully run.

**Return type**

`bool`

### executor

<span id="qiskit_aer.jobs.AerJob.executor" />

`AerJob.executor()`

Return the executor for this job

### in\_final\_state

<span id="qiskit_aer.jobs.AerJob.in_final_state" />

`AerJob.in_final_state()`

Return whether the job is in a final job state such as `DONE` or `ERROR`.

**Return type**

`bool`

### job\_id

<span id="qiskit_aer.jobs.AerJob.job_id" />

`AerJob.job_id()`

Return a unique id identifying the job.

**Return type**

`str`

### qobj

<span id="qiskit_aer.jobs.AerJob.qobj" />

`AerJob.qobj()`

Return the Qobj submitted for this job.

**Returns**

the Qobj submitted for this job.

**Return type**

[Qobj](qiskit.qobj.Qobj "qiskit.qobj.Qobj")

### result

<span id="qiskit_aer.jobs.AerJob.result" />

`AerJob.result(timeout=None)`

Get job result. The behavior is the same as the underlying concurrent Future objects,

[https://docs.python.org/3/library/concurrent.futures.html#future-objects](https://docs.python.org/3/library/concurrent.futures.html#future-objects)

**Parameters**

**timeout** (*float*) – number of seconds to wait for results.

**Returns**

Result object

**Return type**

qiskit.Result

**Raises**

*   **concurrent.futures.TimeoutError** – if timeout occurred.
*   **concurrent.futures.CancelledError** – if job cancelled before completed.

### running

<span id="qiskit_aer.jobs.AerJob.running" />

`AerJob.running()`

Return whether the job is actively running.

**Return type**

`bool`

### status

<span id="qiskit_aer.jobs.AerJob.status" />

`AerJob.status()`

Gets the status of the job by querying the Python’s future

**Returns**

The current JobStatus

**Return type**

[JobStatus](qiskit.providers.JobStatus "qiskit.providers.JobStatus")

**Raises**

*   [**JobError**](qiskit.providers.JobError "qiskit.providers.JobError") – If the future is in unexpected state
*   **concurrent.futures.TimeoutError** – if timeout occurred.

### submit

<span id="qiskit_aer.jobs.AerJob.submit" />

`AerJob.submit()`

Submit the job to the backend for execution.

**Raises**

*   **QobjValidationError** – if the JSON serialization of the Qobj passed
*   **during construction does not validate against the Qobj schema.** –
*   [**JobError**](qiskit.providers.JobError "qiskit.providers.JobError") – if trying to re-submit the job.

### wait\_for\_final\_state

<span id="qiskit_aer.jobs.AerJob.wait_for_final_state" />

`AerJob.wait_for_final_state(timeout=None, wait=5, callback=None)`

Poll the job status until it progresses to a final state such as `DONE` or `ERROR`.

**Parameters**

*   **timeout** (`Optional`\[`float`]) – Seconds to wait for the job. If `None`, wait indefinitely.

*   **wait** (`float`) – Seconds between queries.

*   **callback** (`Optional`\[`Callable`]) –

    Callback function invoked after each query. The following positional arguments are provided to the callback function:

    *   job\_id: Job ID
    *   job\_status: Status of the job from the last query
    *   job: This BaseJob instance

    Note: different subclass might provide different arguments to the callback function.

**Raises**

[**JobTimeoutError**](qiskit.providers.JobTimeoutError "qiskit.providers.JobTimeoutError") – If the job does not reach a final state before the specified timeout.

**Return type**

`None`

## Attributes

<span id="qiskit_aer.jobs.AerJob.version" />

### version

`= 1`
