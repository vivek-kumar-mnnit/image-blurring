# Image Processing using Verilog

## Overview

This project aims to perform image blurring on a grayscale image using a Gaussian Kernel of size 5x5. The entire implementation is done using Verilog in Xilinx ISE/Vivado. The project was presented at the Avishkar 2024 Technical Fest at our college, where we were the Runner up.

## Project Objective

- **Task:** Operate to blur a given grayscale image of size 12x12 pixels.
- **Pixel Values:** Each pixel can have a decimal intensity value from -128 to 127 (-128 being black and 127 being white).
- **Kernel Used:** Gaussian Kernel of size 5x5.
- **Storage:** The image is stored and modified in a RAM of size 144 Bytes.
- **Design Approach:** The data path and Controller design approach is used to implement this operation.

## Implementation Details

1. **Image Storage:**
   - The 12x12 grayscale image is stored in a RAM of size 144 Bytes. Each pixel's intensity value is stored as an 8-bit signed integer.

2. **Gaussian Kernel:**
   - The Gaussian Kernel used for blurring is of size 5x5. The weights of the kernel are predefined and are used to convolve with the image to produce the blurred effect.

3. **DataPath and Controller:**
   - The design is divided into two main components: DataPath and Controller.
   - **DataPath:** Handles the data operations such as reading the pixel values from RAM, performing the convolution with the Gaussian Kernel, and writing back the modified pixel values.
   - **Controller:** Manages the sequence of operations, ensuring that the DataPath executes the steps in the correct order.

## Verilog Modules

The project consists of several Verilog modules that work together to achieve the image-blurring effect.

### Top Module
The top module initializes the RAM with the image data, instantiates the DataPath and Controller modules, and manages the overall operation flow.




```Verilog
module top_module;
    // Code for the top module
end module
```
### DataPath Module
The DataPath module performs the core image processing operations. It reads pixel values, applies the Gaussian Kernel, and stores the results back into RAM.


```Verilog
module datapath;
    // Code for the DataPath module
end module
```
### Controller Module
The Controller module sequences the operations, controlling when the DataPath reads, processes, and writes data.


```Verilog
module controller;
    // Code for the Controller module
end module
```
### RAM Module
The RAM module stores the image data. It supports read and write operations required for image processing.


```Verilog
module ram;
    // Code for the RAM module
end module
```
### Simulation and Testing
The design was simulated and tested using Xilinx ISE/Vivado to ensure that the image blurring operation works correctly. Testbenches were written to validate each module and the overall system.

### Results
The project successfully blurred the 12x12 grayscale image using the Gaussian Kernel. The implementation met all design requirements and was verified through simulation.

### Conclusion
This project demonstrated an effective approach to image processing using Verilog. The combination of DataPath and Controller design allowed for efficient handling of the image blurring task.

### Acknowledgments
We would like to thank our college and the organizers of Avishkar 2024 for allowing us to present our work. Special thanks to our mentors and peers for their support and guidance.



![image](https://github.com/RBSuhail/fpga/assets/114150506/1ea8341b-5804-4c24-888f-a10a15a8f9bd)
### Gaussian mask
![image](https://github.com/RBSuhail/fpga/assets/114150506/c6ab6701-28bc-4c26-be4c-7eadd7a054bc)
![image](https://github.com/RBSuhail/fpga/assets/114150506/7daed31e-c4e1-4f2b-8246-af858ec5001c)

### Convolution operation
![image](https://github.com/RBSuhail/fpga/assets/114150506/05d621fb-7f32-442e-a79b-90e6d3279eba)
![image](https://github.com/RBSuhail/fpga/assets/114150506/94b606b0-d6f6-4674-8410-e12461b8e0cc)

![image](https://github.com/RBSuhail/fpga/assets/114150506/b1289e03-e6c4-4b56-8af5-c036c1d1dd7c)

### State Diagram
![image](https://github.com/RBSuhail/fpga/assets/114150506/84e47232-ee48-453d-aefa-32d659af66eb)
![image](https://github.com/RBSuhail/fpga/assets/114150506/8b5db831-f4ae-4669-92a7-79c1feba5fe1)
### Booth Multiplier
![image](https://github.com/RBSuhail/fpga/assets/114150506/3af9b16d-6824-4ea1-80a2-e559e1637b03)
![image](https://github.com/RBSuhail/fpga/assets/114150506/b07eacf8-6f3d-4b0b-b14d-a6c0b59c6485)
