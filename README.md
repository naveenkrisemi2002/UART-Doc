# UART-Doc
To understand the concept of UART practically, it is important to note that even though 
the transmitter (TX module), receiver (RX module), and baud rate generator exist 
within a single UART chip, actual data transfer occurs between two separate UARTs. The 
TX module of one UART transmits data to the RX module of another UART. 
For simulation (verification), it is not possible to test both transmission and reception 
using a single top module. A top module is required only for synthesis (i.e., hardware 
implementation). 
If you want to simulate both transmission and reception, you need to use two 
UARTs—one UART's TX module will send data to the second UART's RX module. This 
introduces several synchronization challenges that need to be resolved. Such testing is 
typically performed at the block level verification stage rather than at the system level.
