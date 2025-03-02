
# Cyber Systems - Assignment 1
**Group 2**  
This project implements a **Finite State Machine with Datapath (FSMD) Simulator**, capable of processing different **XML test descriptions** and **stimulus files** to execute various FSMD tasks. The simulator reads a finite-state machine description and executes transitions based on conditions and operations.


### Usage
- The core simulator is implemented in `fsmd-sim.py`, which remains the same for all tasks.
- All simulations run **until the conversion is complete** or when cycles run out, so **a large cycle count** (e.g., **100** or larger) in the bash command is recommended to ensure everything finishes properly.  
**Remember to replace [integer]** with an appropriate value.
- Each task is defined using an **FSMD description file** (`*_desc.xml`) and **stimulus file** (`*_stim.xml`)

## Tasks
### Task 1
Task 1 starts by initializing var_A and var_TH (variables), then enters the COMPUTE state where it decrements var_A until it equals var_TH, at which point the FSM transitions to the DONE state. No external inputs are used in this test. To start Task 1, execute:

```python3 fsmd-sim.py [integer] test_2/gcd_desc.xml test_2/gcd_stim.xml```  
```python3 fsmd-sim.py 100 test_1/test_desc.xml```

### Task 2
Task 2 simulates the computation of the GDC of two numbers until both values become equal or the number of cycles end.


To run the simulation, modify the inputs in `gcd_stim3.xml`.  
Before running the simulation, modify the inputs `in_A` and `in_B` inside the file `test_2/gcd_stim.xml`. Then execute:


```python3 fsmd-sim.py [integer] test_2/gcd_desc.xml test_2/gcd_stim.xml```  
```python3 fsmd-sim.py 100 test_2/gcd_desc.xml test_2/gcd_stim.xml```


### Task 3
Task 3 is an **Integer to Binary Converter** simulator. It takes the following inputs:
- `number` - integer to convert
- `in_bits` - the number of bits for the binary representation (auto-adjusts if too low).

The simulation runs until the conversion is complete, so **a larger cycle count** might be needed (try 1000). It will ensure the task finishes properly. To run the simulation, modify the inputs in `gcd_stim3.xml`, then execute:

```python3 fsmd-sim.py [integer] gcd_desc3.xml gcd_stim3.xml```  
```python3 fsmd-sim.py 1000 gcd_desc3.xml gcd_stim3.xml```

**Important Note on Task 3**  
Due to XML file limitations, the output will display 8s instead of 0s in the binary representation. The actual values should be interpreted as if 8 = 0.



Thanks!  
Group 2