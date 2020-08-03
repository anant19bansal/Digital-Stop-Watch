# Digital-Stop-Watch
We designed a stop watch with 4 digit display showing seconds and 1/100 second. A push button was used to go through a cycle of three states, viz. RESET, START and STOP sequentially.
### Hardware and ICs used :
  - LM555 timer
  - 7414 (Schmitt Trigger)
  - 7473 (JK Flip Flop)
  - 74160 (Synchronous Decade Counter)
  - 7447 (BCD to 7 Segment Decoder)
  - 7 segment LED displays
<img src="https://github.com/anant19bansal/Digital-Stop-Watch/blob/master/Hardware%20and%20ICs%20used.jpg" width="50%" height="50%">  

## Clock Generation:
555 timer IC was configured in astable multivibrator mode to generate the clock with time period approximately equal to 10ms. 
