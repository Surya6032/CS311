time/program=time/cycle * cycle/instruction*instructions/program
* It should be independent of machine.
CPU bound - the task is most constrained by the CPU.
Memory bound- the task is most constrained by the amount of memory available.
I/O bound - the task is most constrained by the I/O subsystem.

## Compairing Hardware
* Benchmarks
    (Poor things to measure hardware performance)
    Clock rate
    MIPS - millions of instructions per second.
    FLOPS - Floating point operations per second.

### Synthetic Benchmarks
* Whetstone - a floating point computational suite
* Drystone - an integer computational suite
* Linpack - another floating point computational suite.


### SPEC - Standard performancce evaluation corporation (Organization created by computer hardware companies)http://spec.org/

### CPU optimization 
* Cahcing
* Instruction pipelining
* Specialized execution units
* parallel execution units
* branch prediction
* code optimization

#### Delayed branching
#### Branch prediction
#### Speculative exceution
#### Loop optimization


Example:- 
* LOOP:
  * SUB   R3, R3,  R1
  * STORE R3, O(R5)
  * STORE R4, 0(R6)
  * BNEZ  R3  LOOP
*               1     2     3      4     5        6        7      8
* SUB R3,R3,R1:Fetch decode, data, exec,store
* STORE R3, O(R5):   Fetch, data,  decode,exec,store
* STORE R4, 0(R6):          Fetch, data,   decode,exec,  store 
* BNEZ  R3  LOOP:                  Fetch,  data,   decode, exec, store
* (Better Option)

* LOOP:
  * SUB   R3, R3,  R1
  * BNEZ  R3  LOOP
  * STORE R3, O(R5)
  * STORE R4, 0(R6)
  
* Branch prediction

  
