Problems what occurred in the current committee in uart_proj branch:
1. Led connected to PC13 is always turned on. But if is_set boolean variable change to opposite value in each loop step, the led is toggling.
SOLVED: PC13 was configured as an Open Drain output, so 0 means led is turned on and vice versa.
2. TX and RX in loop are working fine, but in interruption is a problem.