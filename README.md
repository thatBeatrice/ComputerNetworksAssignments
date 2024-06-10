Python solutions for Computer Networks' assignments.

## [Token Ring](TokenRing.ipynb)
This code simulates a network of calculators that can send messages to each other. The network is implemented as a circular list of Calculator objects, each with a unique IP address generated randomly within the valid range (0-255).

- *Random IP Generation:* Each calculator is assigned a random IP address using the generate_random_IP function.
- *Circular Network:* The network is structured as a circular list, ensuring messages eventually reach their destinations.
- *Token-Based Communication:* A Token object is used to encapsulate the message, source IP, destination IP, and flags indicating delivery status and busy state.
- *Message Transmission:* The transmit_message function handles token movement through the network:
  - Locates the source calculator.
  - Moves the token through the network until it reaches the destination calculator.
  - Appends the message to the destination calculator's buffer.
  - Returns the token back to the source calculator.
- *Network Visualization:* The print_network function displays the IP address and message buffer of each calculator in the network.
- *Interactive Message Creation:* The move_token function allows users to input messages for transmission, simulating user interaction with the network.


## [Two Dimensional Parity Bits and Cyclic Redundancy Check](2DParityBitsAndCRC.ipynb)
**Two-Dimensional Parity Bits**: This method adds parity bits to a two-dimensional array of data (matrix) to detect errors in both rows and columns.

**Cyclic Redundancy Check (CRC)**: This method calculates a checksum (CRC value) based on the message and a generating polynomial. The receiver calculates the CRC value again and compares it with the transmitted one to detect errors.

- *Two-Dimensional Parity Bits:*
  - Calculates parity bits for both rows and columns of the data matrix.
  - Simulates an error in the matrix.
  - Locates the position (row and column) of the flipped bit.

- *Cyclic Redundancy Check:*
  - Checks for valid message and generating polynomial lengths.
  - Pads the message with zeros to match the generating polynomial length.
  - Performs XOR operations to calculate the CRC value.
  - Verifies the received message by calculating the CRC value again and comparing it with the transmitted one.
