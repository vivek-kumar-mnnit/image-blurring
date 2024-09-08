`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 15.03.2024 10:20:09
// Design Name: 
// Module Name: BRAM_2
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


module BRAM_2(clk,MX2,MY2,rd_v,image_out ,i,j);

input clk,i,j;
input [3:0] MX2,MY2;
input rd_v;
output [7:0] image_out;
reg [7:0] image_mat[11:0][11:0]=

{
{3, 8, 11, 8, 3, 3, 8, 11, 8, 3, 1, 3},
{4, 11, 14, 11, 4, 4, 11, 14, 11, 4, 4, 11},
{1, 3, 4, 3, 1, 1, 3, 4, 3, 1, 1, 3},
{3, 8, 11, 8, 3, 3, 8, 11, 8, 3, 3, 8},
{1, 3, 4, 3, 1, 1, 3, 4, 3, 1, 1, 3},
{3, 8, 11, 8, 3, 3, 8, 11, 8, 3, 1, 3},
{4, 11, 14, 11, 4, 4, 11, 14, 11, 4, 4, 11},
{1, 3, 4, 3, 1, 1, 3, 4, 3, 1, 1, 3},
{3, 8, 11, 8, 3, 3, 8, 11, 8, 3, 3, 8},
{1, 3, 4, 3, 1, 1, 3, 4, 3, 1, 1, 3},
{3, 8, 11, 8, 3, 3, 8, 11, 8, 3, 1, 3},
{4, 11, 14, 11, 4, 4, 11, 14, 11, 4, 4, 11}
};
always @(posedge clk) begin
if(rd_v)begin

//image_out<=image_mat[MX2][MY2][7:0];
end
end
endmodule
