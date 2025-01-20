# FPGA-Based-High-speed-Mutliplier-design-using-Kogge-stone-adder
• Kogge-stone adder employed for High speed Multiplication through Parallel adders of partial products . • With this user-friendly application, you can effortlessly organize and efficiently design high speed multipliers. • Tools And technologies used: Xilinx ISE, Verilog Programming

# code
module mul8bit(
 input [7:0] x,y,
 output [15:0] z
 );
wire [7:0] pa0,pa1,pa2,pa3,pa4,pa5,pa6,pa7;
wire [15:0] fa0,fa1,fa2,fa3,fa4,fa5,fa6,fa7;
wire [16:0] op1,op2,op3,op4,op5,op6;
wire c;
assign pa0[0]= y[0] & x[0];
assign pa0[1]= y[1] & x[0];
assign pa0[2]= y[2] & x[0];
assign pa0[3]= y[3] & x[0];
assign pa0[4]= y[4] & x[0];
assign pa0[5]= y[5] & x[0];
assign pa0[6]= y[6] & x[0];
assign pa0[7]= y[7] & x[0];
assign pa1[0]= y[0] & x[1];
assign pa1[1]= y[1] & x[1];
assign pa1[2]= y[2] & x[1];
assign pa1[3]= y[3] & x[1];
assign pa1[4]= y[4] & x[1];
assign pa1[5]= y[5] & x[1];
assign pa1[6]= y[6] & x[1];
assign pa1[7]= y[7] & x[1];
assign pa2[0]= y[0] & x[2];
assign pa2[1]= y[1] & x[2];
assign pa2[2]= y[2] & x[2];
assign pa2[3]= y[3] & x[2];
assign pa2[4]= y[4] & x[2];
assign pa2[5]= y[5] & x[2];
assign pa2[6]= y[6] & x[2];
assign pa2[7]= y[7] & x[2];
assign pa3[0]= y[0] & x[3];
assign pa3[1]= y[1] & x[3];
assign pa3[2]= y[2] & x[3];
assign pa3[3]= y[3] & x[3];
assign pa3[4]= y[4] & x[3];
assign pa3[5]= y[5] & x[3];
assign pa3[6]= y[6] & x[3];
assign pa3[7]= y[7] & x[3];
assign pa4[0]= y[0] & x[4];
assign pa4[1]= y[1] & x[4];
assign pa4[2]= y[2] & x[4];
assign pa4[3]= y[3] & x[4];
assign pa4[4]= y[4] & x[4];
assign pa4[5]= y[5] & x[4];
assign pa4[6]= y[6] & x[4];
assign pa4[7]= y[7] & x[4];
assign pa5[0]= y[0] & x[5];
assign pa5[1]= y[1] & x[5];
assign pa5[2]= y[2] & x[5];
assign pa5[3]= y[3] & x[5];
assign pa5[4]= y[4] & x[5];
assign pa5[5]= y[5] & x[5];
assign pa5[6]= y[6] & x[5];
assign pa5[7]= y[7] & x[5];
assign pa6[0]= y[0] & x[6];
assign pa6[1]= y[1] & x[6];
assign pa6[2]= y[2] & x[6];
assign pa6[3]= y[3] & x[6];
assign pa6[4]= y[4] & x[6];
assign pa6[5]= y[5] & x[6];
assign pa6[6]= y[6] & x[6];
assign pa6[7]= y[7] & x[6];
assign pa7[0]= y[0] & x[7];
assign pa7[1]= y[1] & x[7];
assign pa7[2]= y[2] & x[7];
assign pa7[3]= y[3] & x[7];
assign pa7[4]= y[4] & x[7];
assign pa7[5]= y[5] & x[7];
assign pa7[6]= y[6] & x[7];
assign pa7[7]= y[7] & x[7];
assign fa0 = {8'b00000000, pa0};
assign fa1 = {7'b0000000, pa1,1'b0};
assign fa2 = {6'b000000, pa2,2'b00};
assign fa3 = {5'b00000, pa3,3'b000};
assign fa4= {4'b0000, pa4,4'b0000};
assign fa5 = {3'b000, pa5,5'b00000};
assign fa6 = {2'b00, pa6,6'b000000};
assign fa7 = {1'b0, pa7,7'b0000000};
endmodule
