# G07
from microbit import *

started = False
while True:
    
    if button_a.is_pressed():
        started = True
    elif button_b.is_pressed():
        started = False
    while started:
      reading = pin1.read_digital()
      if reading == 1:
          pin2.write_digital(1)
          pin0.write_analog(1000)
    
      if button_b.is_pressed():
          pin2.write_digital(0)
          pin0.write_analog(0)
          break
                
                        
                        
            
        
        
    
    
