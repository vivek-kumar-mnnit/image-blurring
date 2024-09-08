`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 15.03.2024 10:24:34
// Design Name: 
// Module Name: CONTROL
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


module CONTROL(clk,rst,sop_fait,sop_in,rd_v,MX1,MY1,MX2,MY2,,i,j,fil_image ,done);
        input clk,rst,sop_fait,sop_in;
        output reg rd_v;
        output reg done;
        output reg [2:0] MX1,MY1,MX2,MY2;
        output  reg [7:0] fil_image;
        output reg [3:0] i,j;
        parameter image_size=12;
        reg [2:0] state,next_state;
         reg [7:0] temp_image[4:0][4:0]; 
        localparam A=000;
        localparam B=001;
        localparam C=010;
        localparam D=011;
        localparam E=100;
        localparam F=101;
        localparam G=110;
        localparam H=111;
        reg [15:0] count;
        reg [7:0] image_data,kernel_data;
        reg[2:0] TX1,TY1;
         reg[2:0] TX2,TY2;
         reg valid ;
         
         wire [7:0] gauss_data;
   
initial begin
        count<=0;
        state<=0;
        MX1<=0;
        MY1<=0;
        MX2<=j-2;
        MY2<=i-2;
        
        fil_image<=0;
        i<=2;
        j<=2;
end


always @(posedge clk)
begin
        if(rst) begin
        state<=A;
        MX1<=0;
        MY1<=0;
        MX2<=i-2;
        MY2<=j-2;
        fil_image<=0;
        i<=2;
        j<=2;
        
        end
        else 
        state<=next_state;
end



always @(posedge clk)
begin
case(state)
        A: begin next_state<=B;
        rd_v<=1;
        
        end
        B: begin 

        if(rd_v && MX1!=5 && MX2!=j+2 &&MY1!=5 && MY2!=i+2)
        begin
            //BRAM_1 b1 (clk,MX1,MY1,rd_v,kernel_data);
        //    gauss_data<=kernel[MX1][MY1];
          //  BRAM_2 (clk,MX2,MY2,rd_v,image_data ,i,j);
          //  booth_multiplier (clk,rst,rd_v,image_data,gauss_data,valid,temp_image[MX1][MX2]);
        if(MX1==5)begin 
            MX1<=0;
            MY1<=MY1+1'b1;
        end 
        else begin
            MX1<=MX1+1'b1;l
        end
           if(MX2==j+2) begin
            MX2<=0;
            MY2<= MY2+1'b1;
           end
           else
           begin
            MX2<=MX2+1'b1;

           end


        next_state<=B;
        end
        else
         next_state<=C;
        end
        C:begin 
        
        if(count>1000000)begin
        count<=count+1;
        
        end
        state<=D;
        end
        D:begin
        rd_v=0;
        if(count>1000000)begin
      
        next_state<=E;
        end
        else begin
          count<=count+1;
        next_state<=D;
        end
        end
        E:begin
        if(i!=image_size-2 || j!=image_size-2)
        begin
        if(TX1!=5 || TY1!=5)
        begin
        fil_image=fil_image+temp_image[TX1][TY1];
        if(TX1==5) 
        begin
         TX1<=0;
         TY1<=TY1+1'b1;
        end
        else
        begin
            TX1<=TX1+1'b1;
        end
        next_state<=E;
        end
        else if(TX1==5 && TX2==5)
        begin 
            fil_image<=fil_image>>>8;
          BRAM_3(i,j,fil_image);
          next_state<=B;
        end
        if(j==image_size-2)
        begin
            i=i+1;
            j=0;
        end
        else 
        j=j+1;
        end
        else next_state<=F;
        end
       
        F: begin 
            done<=1;
        end

endcase
end



endmodule
