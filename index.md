---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

Welcome to my VGA design project. This report will go through my workings in my project, how I attempted to create the Superman logo, and the serval challenges I encountered along the way.

### **Project Set-Up**
Summarise the project set-up and design flow. Include a screenshot of your own set-up, for example see the image of my Project Summary window below. Guideline 1 short paragraph.
The picture below is a screenshot of the project setup. 

<img src="https://raw.githubusercontent.com/AaronPowderly/fpga-AP/main/docs/assets/images/images.png">

### **Template Code**
The template code we were first given was a simple design that demonstrated how create colour stripes on the VGA based on different RGB values on the current pixel column. The chosen colours are stored in registers and updated every clock cycle unless the reset is active. The registered colours are then sent to the VGA output, which displasy the colour stripes chosen

### **Simulation**
The simulation process invloves the use of Vivado’s built-in XSIM tool. This is used to observe VGA module responds to different column values over time. The simulation helps identify any mistakes in the logic, such as incorrect colour ranges or timing errors. Overall the simulation acts as a testing stage to ensure the VGA behaves as intended once implemented. 
### **Synthesis**
The synthesis process converts the verilog code into representations such as lookup tables, registers, timing summaries and usage reports. Implementation then places and routes the components on the actual FPGA ensuring timing requirements are correct and the design can run on the divice. Any issues such as timing voilations or resource conflicts are flagged so they can be fixed before generating the bitstream.

### **Demonstration**
Perhaps add a picture of your demo. Guideline: 1/2 sentences.

## **My VGA Design Edit**
My chosen idea was pixel art of the Superman logo. At first the idea was complex to me but i decided i wanted challenge myself, the idea was more complex then I first thought. I used online reference match the appropriate colours to match the Superman logo.
### **Code Adaptation**
I first began by changing the code to get an idea of how I could start. I slightly changed the code of the orignal colour stripes just changing one of the colours. I then moved on to focusing on how i wnated my image to look, I changed the background by default to blue to match the Superman logo then created where I wanted put the red of the Superman logo. I then began reasearch and understanding of how I to write the code for creating pixel art of the Superman logo. I struggled to get my head wrapped around the idea of columns and rows, and how to manipulate them. My first idea was to try brute force it, but after a week of struggling to get much results, I had help from another student which helped me understand.
 c 
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
