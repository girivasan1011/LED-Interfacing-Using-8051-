# LED Interfacing Using 8051  
## Aim:
To interface an LED with the 8051 microcontroller and control its operation.
## Apparatus Required:
1.Laptop with Keil uVision software
<br>2.Proteus Design Suite
## Circuit Diagram Setup in Proteus:
1.	Open Proteus and create a new project.
2.	Add the following components from the library:
<br> 8051 Microcontroller (AT89C51)
<br> LED
<br> Resistor (330Ω)
<br> Ground (GND) connection
3.	Connect the LED's anode to P1.0 of the microcontroller through a 330Ω resistor.
4.	Connect the cathode of the LED to GND.
5.	Save the design and proceed to programming in Keil.
## Algorithm:
1.	Configure P1.0 as an output port.
2.	Set P1.0 HIGH to turn ON the LED.
3.	Introduce a delay.
4.	Set P1.0 LOW to turn OFF the LED.
5.	Introduce a delay.
6.	Repeat the process continuously.
## Program:
```
#include<reg52.h> 


sbit LED = P2^0;

void Delay(void);

void main(void)
{
    while(1)
	  { 
	      LED = 0;
		    Delay();
		    LED = 1;
		    Delay();
	  }
}
void Delay(void)
{
    int j;
	  int i;
	  for(i=0;i<10;i++)
	  {
	      for(j=0;j<10000;j++)
		{
		}
	}
}
```
## Output:
<img width="717" height="444" alt="image" src="https://github.com/user-attachments/assets/48a2a44e-1415-4143-9ff3-d881e2824b72" />

## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

