
# Cyber Systems - Assinment 1
**Group 2**


This repository contains the required files and commands to run simulations for computing the **Greatest Common Divisor (GCD)** and **Integer to Binary Conversion** using an FSMD simulator.


### Running the Simulations
Use the following terminal commands to execute the different tasks.  
**Remember to replace [integer]** with an appropriate value.

### Task 1 & 2
Task 1 and 2 simulate the computation of the GDC of two numbers until both values become equal.


The simulation runs until the conversion is complete, so **a large cycle count** (e.g., **1,000,000**) ensures it finishes properly. To run the simulation, modify the inputs in `gcd_stim3.xml`.  
Before running the simulation, modify the inputs `in_A` and `in_B` inside the file `test_2/gcd_stim.xml`. Then execute:


```python3 fsmd-sim.py [integer] test_2/gcd_desc.xml test_2/gcd_stim.xml```
```python3 fsmd-sim.py 100 test_2/gcd_desc.xml test_2/gcd_stim.xml```


### Task 3
Task 3 is an **Integer to Binary Converter** simulator. It takes the following inputs:
- `number` - integer to convert
- `in_bits` - the number of bits for the binary representation (auto-adjusts if too low).

The simulation runs until the conversion is complete, so **a large cycle count** (like in the previous tasks) ensures it finishes properly. To run the simulation, modify the inputs in `gcd_stim3.xml`, then execute:

```python3 fsmd-sim.py [integer] gcd_desc3.xml gcd_stim3.xml```  
```python3 fsmd-sim.py 100 gcd_desc3.xml gcd_stim3.xml```

**Important Note**  
Due to XML file limitations, the output will display 8s instead of 0s in the binary representation. The actual values should be interpreted as if 8 = 0.



Thanks!  
Group 2