# Digital-Stop-Watch
We designed a stop watch with 4 digit display showing seconds and 1/100 second. A push button was used to go through a cycle of three states, viz. RESET, START and STOP sequentially.
### Hardware and ICs used :
  - LM555 timer
  - 7414 (Schmitt Trigger)
  - 7473 (JK Flip Flop)
  - 74160 (Synchronous Decade Counter)
  - 7447 (BCD to 7 Segment Decoder)
  - 7 segment LED displays (Common Anode)
<img src="https://github.com/anant19bansal/Digital-Stop-Watch/blob/master/Hardware%20and%20ICs%20used.jpg" width="50%" height="50%">  

### Clock Generation:
555 timer IC was configured in astable multivibrator mode to generate the clock with time period approximately equal to 10ms. 
<img src="https://github.com/anant19bansal/Digital-Stop-Watch/blob/master/Clock%20using%20555%20timer%20IC.png" width="70%" height="70%">
* Values of external passive components taken :
   * Ra = 100 ohm
   * Rb = 6.8k ohm
   * C = 1 micro farad
   
### Debounce Circuit and FSM :
Debounce circuit was made for the push button using passive components and schmitt trigger to prevent the signal from bouncing due to the vibrations of the plates. 
<img src="https://github.com/anant19bansal/Digital-Stop-Watch/blob/master/Debounce%20and%20FSM.png" width="" height=""><br>
A finite machine was made to change the state of the stopwatch using JK flipflops. The output of debounce circuit was given as clock to the flipflops. RESET(00) -> START(11) -> STOP(10) -> RESET(00)

### Synchronous Decade Counter
For this purpose, four 74LS160A ICs were used to build a synchronous decade counter. 74LS160A is a high speed counter and features a fully independent clock circuit. ENP, ENT and Clear_bar pins of this IC were used to modify the operating mode of the stopwatch. 

<img src = "https://github.com/anant19bansal/Digital-Stop-Watch/blob/master/Synchronous%20BCD%20counter.png" width="80%" height="80%">

### Decoder and 7 Segment Display
The outputs of decade counter were connected to input pins of 4 BCD to 7 segment decoder ICs.<br> 
Finally the ouputs of decoder ICs were fed to the seven segment displays of common anode type.
