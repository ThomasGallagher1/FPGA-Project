---
Layout: Home
Title: FPGA VGA Driver Project
Tags: FPGA VGA Verilog
Categories: Demo
---

Hello Viewer, My name is Thomas Gallagher and this is my 3rd years FPGA VGA Verilog project. This project's aim was to display a graphic using Vivado Verilog using a Basys 3 Development Board. My creation was an image of a penguin and I will be discussing the development and problems faced developing this project.

## **Project Development**
### **Initial Idea's**
Undertaking this project I had many problems and roadblocks that I had to face and adapt to create a fully functional project. These issues I will be discussing further.

### **ATU Security Updates**
Recently ATU have updated their network security to avoid and prevent hacks which could corrupt the University. However, this has created problems for students as some students are randomly targetted for breaching security protocols which is untrue. I was one of these cases. 

The second lab we had in SOC, I opened my project and changed some code and started to run my Synthesis. While running my Synthesis vivado shut down and I lost some progress. However, I ran Synthesis two more times and the issue kept occuring. When I consulted with my Lecturer, she gave me different gateways to combate this unwarranted security defence, however, these were warrented ineffective. 

My Leacturer then conntacted the lead administrator, who worked along side me to stop this unwanted defence. 

Three hours after the initial crash we were able to combate the security defence and allow me to start working on my project, however, the lab had finsihed so I was a week behind already.

<img src ="Screenshot 2024-11-29 134949.png"> 
 

### **Failed Idea's**

As I was a week behind due to the Security measures I had to create and code a design in shorter times than my peers while also creating a project that is unique and complicated, while showing my understanding of the task at hand. 

I decided to create a bouncing DVD logo, that would be a rendition of the old DVD logo when the screen was paused for too long. I was able to create a 50x50 square that changes colour but would just rotate colours not change on a bounce off the screen but the major problem I had was making the square move. I stayed back after classes and late into the evenings researching and applying new techniques, but was unable to move the square.

This lead to the scrapping of this idea. 

<img src ="AYwrUq.gif"> 

I also had the idea to make my penguin spin and dance but I was overly ambitious and it was more challenging and time-intensive then initially anticipated. 

## **Template VGA Design**
### **Project Set-Up**
Summarise the project set-up and design flow. Include a screenshot of your own set-up, for example see the image of my Project Summary window below. Guideline 1 short paragraph.

<img src="Screenshot 2024-11-11 171309.png">

### **Template Code**
Outline the structure and design of the Verilog code templates you were given. What do they do? Include reference to how a VGA interface works. Guideline: 2/3 short paragraphs, consider including screenshot(s).
### **Simulation**
Explain the simulation process. Reference any important details, include a well-selected screenshot of the simulation. Guideline: 1/2 short paragraphs.
### **Synthesis**
Describe the synthesis and implementation processes. Consider including 1/2 useful screenshot(s). Guideline: 1/2 short paragraphs.
### **Demonstration**
Perhaps add a picture of your demo. Guideline: 1/2 sentences.

<img src ="IMG_5512(1).gif">

## **My VGA Design Edit**
I created a penguin designed based on design idea's I researched online and found a YouTube video demenstrating a spinning penguin. I then researched images of pixelated penguins to adapt and base my graphic on. Using the ColourStripes.v code given to us by our Leacturer, I was able to understand and manipulate the code to be able to display the graphic. 

This code had me columns of white and black pixels and manipulate the areas the whcich needed other colours using the rows function to display white and red lines of pixels to create this image. 

<img src="IMG_5611.jpeg">

YouTube video = "FPGA VGA output implement" by TaoTao

### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
Using the ColourStripes.v code block I was able to create an understanding of the design layout, for example by manipulating either of the three colour blocks, red, blue and green, it would create another colour. If I change each line to all zero's it would create a black graphic and if I cghange them to all one's it would create a white graphic.

Using this knowledge and I was able to understand how the columumns and rows work. If I wanted to display eight colours in stripes I would need to divide the columns by 8, so thats 8 into 640 which would be 80 pixels wide per graphic. This was evident in the ColourStripes.v code given to us. However, to understand how to implemnet rows into the function was tricky to understand but I had managed to figure it out.

For example if I wanted to display a small 15x15 white pixel square in the top left corner, I would first create a white column of that size and then create a row to stop end of the column.

This is the code shown:

if(col >= 11'd0 && col <11'd15 && row >= 11'd0 && row < 11'd15)
begin
red_next   <= 4'b1111;
green_next <= 4'b1111;
blue_next  <= 4'b1111;
end

### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.

<img src ="Screenshot 2024-12-02 165928.png"> 
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.

<img src ="Screenshot 2024-12-02 172516.png">

<img src="IMG_56272.jpeg">

<img src="IMG_56262.jpeg">

### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

<img src="IMG_56252.jpeg">
