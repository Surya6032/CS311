### Categories of instruction types:
Data Movement -MOVE,LOAD,POP

Arthimetic operations - affect the flag register,ADD,increment,NEGATE

Boolean logic -affect flag reg,AND,NOT,COMPARE,TEST
Bit Manipulation -SHIFTRIGHT,ROTATe, SET,TOGGELE
I/O -(character and block) , READ, WRITE

Transfer control - JMP, GOTO, RETURN

Special purpose - NOP, CMPS, PREFECTHW, LOCK


ORthogonal - it lacks redundancy, and any instruction can use any register and addressing mode

Addressing - 2big issues are data types and addressing modes.

Data Types: there must be hardware  support for a data type before we can create instructions to operate on the data type

Addressing modes: ohw the address bits are interpreted and used is called the addressing mode.

Immediate addressing - the addr bits represent the value to be operated on(literal)

Effective addressing - the addr bits provide information on how to determine the location of the operand.

Forms of effective addressing:
  * Direct addressing :- the address bits are the address
  * register addressing - the address bits name the register that contains the operand
  * Indirect addressing - The address bits specify a location a location in memory that contains a reference to the operand(pointer)
  * Indirect register addressing - the addr bits name a register which contains a reference to the operand
  * Indexed addressing - address bits are added to an index register that contains a reference to the operand.
  * base displacement addressing - the address bits are added to a base register. The base register contains the starting address.
  
  #### ADD
  #### ADDI -indirect, indexed
  #### ADDB - base displacement
  
  ### CPU - fetch-decode-execute cycle
  1. fetch instruction
  2. decode instruction
  3. compute effective address of operands
  4. fetch operands
  5. execute
  6. store result
  
  ### Pipelining 
  Each step is called a pipeline stage.One way is Instruction level pipeling (ILP)
  
  ### K stage pipeline
      tp  - 1st task:-K x tp
            2nd task:- K x tp +1
            --------------------
           total task=(n-1)x tp
      
      (k*tp)+(n-1)*tp = (k+n-1)tp
      =k+(n-1)
      
      Speedup = time without pipeline/time with pipeline
      
      n(k*tp)
      
      S = n(k*tp)/(k+n-1)tp= k*tp/tp=k
      (Only theoretical)
 
 ### Pipeline Conflicts(3 -Types)
 1. Resource conflict(Structural hazard)
 2. data dependency
 3. Conditional branch statements
 
 ### Memory 
 
 To deal with the fact that memory is orders of magnitude slower than the CPU, we create a memory hierarchy of different types of memory.
 
 #### RAM - Random Access Memory, read/write, volatile
 #### ROM - Read only memory, non volatile
 
 #### Two common types of RAM
 1) Dynamic RAM (DRAM) - built with capacitors, must be refreshed often
 2) Static RAM (SRAM) - built with flip flops, retains content as long as it is powered
  
#### 5 Types of ROMS
1) ROM -data/program is fabricated into the chip and cannot be changed.
2) PROM - programmable ROM has fuses that are blown to program the chip, one time programming.
3) EPROM - erasable PROM, can be reprogrammed with UV light, erase entire chip and program it
4) EEPROM - electrically erasable PROM, they can be erased and reprogrammed by byte, no special equipment.
5) Flash Memory - an EEPROM where we can read and write by block(faster than EEPROM)
