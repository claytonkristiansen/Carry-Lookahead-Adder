# Carry-Lookahead-Adder

Objectives:
In this lab I will be creating a carry lookahead adder using structural and dataflow Verilog. The lab will start with a 4-bit carry lookahead adder and finish with a 2-level 16-bit carry lookahead adder. Components from the 4-bit carry lookahead adder are used to create the 2-level 16-bit carry lookahead adder. The delays for each of the adders and how they compare to carry ripple adders will also be determined. This lab will provide valuable experience working with carry lookahead adders and understanding the impact of more efficient circuit designs on delay.

Results:	
The generate/propagate, carry lookahead, and summation units combined properly to create the 4-bit carry lookahead adder. The resulting waveform with delays showed the delay to be 8ns. The aforementioned units were combined with the block carry lookahead unit to create the 16-bit 2-level carry lookahead adder. This adder functioned properly, passed all the test, and the waveform illustrated that the delay was 16ns.

Conclusion:
In this lab I gained valuable experience creating a carry lookahead adder using Verilog. I also gained a deeper understanding of the impact of using more efficient gate designs to reduce the overall delay. Reducing this delay allows the circuit to be driven at a higher clock speed which is useful because you can process more information in a smaller amount of time. Creating the modules for the lookahead adders was the most challenging aspect of this lab because the indices of the carry bits were not straightforward in how they were set up. The carry bits for the carry lookahead unit were offset to the left by one because the carry in bit needed to occupy the C[0] bit. Both the 4-bit and 16-bit carry lookahead adders worked as intended and passed all of the testbench tests. 







Questions:
2-3b) Did the delay of the 16-bit 2-level carry lookahead adder match the computed delay from the pre-lab?
	Unfortunately, I miscalculated the delay in the prelab and computed a 14ns delay when the real delay was 16ns. 
4) How does the gate-count of the 16-bit carry lookahead adder compare to that of a ripple carry adder of the same size?
	By counting up all the logical operators in my Verilog code for the 16-bit 2-level carry lookahead adder I found that there are 190 gates used to add two 16-bit numbers. Likewise, I found that there are 80 gates used to add 16-bit number in a full carry-ripple adder. There are less gates used in large number addition using carry-ripple adders, but more time required to add them.
5) How does the propagation delay of the 4-bit carry lookahead adder compare to that of a ripple-carry adder of the same size?
	The propagation delay of the 4-bit carry lookahead adder was 8ns, whereas the delay of a ripple-carry adder of the same size would have a 20ns delay because the carry bits must propagate through each full adder in series before the add operation is complete.
How does the propagation delay of the 16-bit carry lookahead adder compare to that of a ripple carry adder of the same size?
	The propagation delay of the 16-bit 2-level carry lookahead adder was 16ns, whereas the delay of a ripple carry adder of the same size would be 80ns because of the dependency each succeeding bit has on the bit before it.
