### Parallel and Multiprocessor

#### Superscalar processor
1. superpipelining: where each pipelining in which tasks are completed in half clock cycle.
2. Fetch multiple instruction at a time:- Fetch multiple instruction from the memory.
3. complex decode unit that can detect dependencies
4. additional specialized circuitry called execution units.
#### VLIW - Very long instruction word
Combine multiple instruction and add them to a word.
IA-64 ISA

#### Vector processor
* load vector A from memory into a vector register
* load vector B from memory into a vector register
* vector add A and B
* store the result to memory

#### Interconnection network
* Each process has its own memory and other process can also use that memory.
* bandwidth - information carrying capacity of the network
* message latency- how long it takes for the first bit of message to arrive (propogation delay)
* Transport latency - how long it takes the entire message to cross the network (transmit time)
* Overhead -  work required by the sender and receiver to connect and process messages.


#### Static networks - connections are fixed and may not change

#### Dynamic network - connection may be created and destroyed as needed.

#### Non blocking - new connections are allowed with existing connections(no wait)

#### Blocking- new connections are not allowed until the current connection is complete(must wait)

#### Topologies  (how can we connect nodes together)
* Path (linear): P--P--P--P
* Ring (loop):
                      P--p
                      |  |
                      p--p
                      
Star(hub): 
              P   P
              \  /
            P--P--P
              /  \
             P    P

* Tree : an acycllic network with a single distinguished node called the root.
* Mesh: each node is connected to its neighbors on a 2D or 3D grid.

* Hypercube
* Full mesh
