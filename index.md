---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

Welcome to my VGA design project. This report will go through my workings in my project, how I attempted to create the Superman logo, and the serval challenges I encountered along the way.

### **Project Set-Up**
This is my Vivado project summary it shows the build status and configuration of the FPGA design for the Artix 7 device. Synthesis is marked with a few warnings, while implementation has successfully completed routing with only two warnings. It also lists project settings such as the top-level module VGATop. The project is fully configured, and the last implementation run has completed without critical issues. The summary is for an overview of build progress, to help verify that the design flow has been completed correctly before generating the final bitstream. 
<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/Project_Summary.png">

### **Template Code**
The template code we were first given was a simple design that demonstrated how create colour stripes on the VGA based on different RGB values on the current pixel column. The chosen colours are stored in registers and updated every clock cycle unless the reset is active. The registered colours are then sent to the VGA output, which displasy the colour stripes chosen

### **Simulation**
The simulation process invloves the use of Vivado’s built-in XSIM tool. This is used to observe VGA module responds to different column values over time. The simulation helps identify any mistakes in the logic, such as incorrect colour ranges or timing errors. Overall the simulation acts as a testing stage to ensure the VGA behaves as intended once implemented. 
### **Synthesis**
The synthesis process converts the verilog code into representations such as lookup tables, registers, timing summaries and usage reports. Implementation then places and routes the components on the actual FPGA ensuring timing requirements are correct and the design can run on the divice. Any issues such as timing voilations or resource conflicts are flagged so they can be fixed before generating the bitstream.

### **Implementation**
<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-F6722851-5406-47C7-BFF0-1C1596C9265E.jpeg" width=50%>

### **Demonstration**
This is an image of my demonstration. This shows it running on my Basys3 board therefore showing that my VGA design runs as expected on the hardware.

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-CB95B7F3-1FFA-4C42-BFEE-13DB14E70AB4.jpeg" width=50%>

## **My VGA Design Edit**
My chosen idea was pixel art of the Superman logo. At first the idea was complex to me but i decided i wanted challenge myself, the idea was more complex then I first thought. I used online reference match the appropriate colours to match the Superman logo.
<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/images.png" width=105%>
### **Code Adaptation**
I first began by changing the code to get an idea of how I could start. I slightly changed the code of the orignal colour stripes just changing one of the colours. I then moved on to focusing on how i wnated my image to look, I changed the background by default to blue to match the Superman logo then created where I wanted put the red of the Superman logo. I then began reasearch and understanding of how I to write the code for creating pixel art of the Superman logo. I struggled to get my head wrapped around the idea of columns and rows, and how to manipulate them. My first idea was to try brute force it, but after a week of struggling to get much results, I had help from another student which helped me understand.
I drew out at half a page of 640x480 grid, and marked down the boxes and layout of how i wanted my project to look. This really helped adapt the code for the columns and rows, I divided each square by 16. So for each 16 row and columns I would designate it a colour example row 207 to 223 and column 127 to 143 is designated black for the outline. 

[1]
<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-75B37590-DCDD-4AC7-A77F-EDCCF844C32F.jpeg" width=50%>

### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
The image below shows the schematic after the synthesis of FPGA design created by Vivado, showing the logical structure made after the code is synthesized into the hardware.
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-01D0E260-A425-4606-AFCF-83B27FFCC2A0.jpeg" width=50%>

### **Demonstration**
- This is the Basys3 board I used. 

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-69FFF612-822D-4BA8-A1E7-94C9AE4B437E.jpeg" width=50%>

- This is my first change in code, just changing one of the colour in the orignal code of the colour stripes.

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-8EDC1D43-4007-4DA3-B010-C2E64787F44F.jpeg" width=50%>

- Then I began with setting the background colour to blue decided where i wnated the red background as well.

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-293092FA-7817-4119-A3B0-0FBF2C78E6F7.jpeg" width=50%>

- Beginning of the outline of the Superman Logo.

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-390987BD-60FF-429E-8AEE-E81CB86BD918.jpeg" width=50%>

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-7E5E5851-E559-43D4-9B33-2FF9E098B6CE.jpeg" width=50%>

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/processed-CB95B7F3-1FFA-4C42-BFEE-13DB14E70AB4.jpeg" width=50%>

## **References**
[1] PixilArt, Used as inspiration for my design, Available Online: [Superman Logo](https://www.pixilart.com/draw/the-superman-logo-066188a624)

[2] ChatGPT, Used to help understand Simulation and Synthesis, Available Online: [ChatGPT](https://chatgpt.com/)



