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
  
  
