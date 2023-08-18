# CS-350-Emerging-Systems-Architecture-and-Technology

•	Summarize the project and what problem it was solving.
 o For this project we used a Texas Instruments SimpleLink Wi-Fi CC3220s Launchpad development kit and we were asked to modify the gpiointerupt.c file and develop a program in C language using a 
   task scheduler and timer to do the following:
  o  	Check for button presses on the launch pad board every 200ms
  o  	Check the temperature sensor on the board for current temperature value every 500ms using the I2C function
  o	  Update the LED to turn off or on when heat or no heat is indicated using GPIO_Write
  o  	If you push the decrease button it decreases the threshold or setpoint value of the temperature by 1 degree every 200ms using the GPIO interrupt callback
  o	  If you push the increase button it increases the threshold or setpoint value of the temperature by 1 degree every 200ms using the GPIO interrupt callback
  o	  If the temperature is less than the setpoint or threshold value, then the LED light turns on (controlling a heater)
  o	  If the temperature is greater than the setpoint or threshold value, then the LED light turns off.
  o	  output to the server(via UART) every 1 second or 1000ms in this format: DISPLAY(snprintf(output, 64, "<%02d,%02d,%d,%04d>\n\r", temperature, setpoint, heat, seconds))
  
•	What did you do particularly well?
 o I think I utilized the task scheduler, UART, gpio interrupt callback, and the GPIO_write functions appropriately. Everything worked exactly as intended and I successfully implemented all 
    requirements. This was my first attempt at completing something of this magnitude. While challenging, I learned a lot  from this class and I’m proud of my accomplishments.
    
•	Where could you improve?
 o	I believe I could have done better using the timer, although everything was functional exactly as required, I should have changed my period time and that would have improved my callback times.
 
•	What tools and/or resources are you adding to your support network?
 o	I have never worked on a project that was in C language. That alone was challenging, but it gave me insight to another language I hadn’t experienced before. Additionally, having had this 
    experience working with an embedded system firsthand, I am going to further explore this field for future experiences. 
    
•	What skills from this project will be particularly transferable to other projects and/or course work?
 o	Learning about embedded systems and how they affect us in the world today was interesting. I come from a medical background of being a nurse for the past 11 years. Embedded systems were all 
    around me and having had this experience I am able to see a new perspective of the medical field and how it can be improved for both medical staff and patient experiences.
    
•	How did you make this project maintainable, readable, and adaptable?
 o	When I developed this project, I made sure to use reusable code utilizing the task handler to call the functions necessary at various times with a timer. I made sure that I eliminated all 
    unnecessary white space and thoroughly commented my code from start to finish. I also included a problem at the top explaining the contents of the project and the requirements. I then added a 
    solution comment section explaining how I met all of the requirements I listed in the problem, and what functions were called at individual times, and the actions they held.
