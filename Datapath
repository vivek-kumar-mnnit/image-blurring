`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 15.03.2024 10:25:09
// Design Name: 
// Module Name: DATAPATH
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module DATAPATH(clk,rst,gauss_data ,image_in,image_out,sop_fait,sop_in );
output sop_fait,sop_in;
input clk,rst,gauss_data,image_out;
BRAM_1(clk,MX1,MY1,rd_v,gauss_data );
BRAM_2(clk,MX2,MY2,rd_v,image_out ,i,j);
BRAM_3(i,j,fil_image);

always @(posedge clk) begin
end
endmodule
