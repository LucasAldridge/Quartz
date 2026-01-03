tommy gave me his Dell Poweredge R720. this thing is so cool but it is also so shit. it is big and loud and i will not use it in its current state. it does, however, have 16 SAS drive bays.  SAS drives are very cheap. I like cheap storage. What i desire is JUST the drive bays and the backplane. **I want to be able to connect the bays and backplane to any other computer and that computer have infinite storage.

I am to understand that this is possible. there are 4 mini SAS connectors on the backplane, one proprietary dell power cable, and one cable that controls some LEDs relating to the drives that i do not care about at all. 

what this means is i need to 
1.  reverse engineer the pin-out for this proprietary power cable and create an adapter so that i can power the drives with other shit. 
2.  connect the mini SAS cables to a PCIE-->SAS HBA installed on the other computer
## Powering the drives
---
the "proprietary" Dell cable is really fuckin simple. its a 4x2 connector but only 6 of the connectors are relevant. there's 3 12V pins (yellow wires on the dell conector), 3 ground pins (black wires on dell connector), and the other two are proprietary and unneccesary. chatGPT is saying i need a roughly 20A power supply for 8 drives if they all spun up at once, and im def fine if i can stagger spinup on the drives. chat loves to say a bunch of BS and i really think im chillin off a 12V 20A PSU if my HBA lets me stagger spinup. im js gonna do it and not stress too hard. 

due to power demand i have decided im js gonna do 1 backplane of 8 drives. 

this idea has been near fully explored other than actually doing, which i will do shortly. 

TLDR: 

- get a dell r730 backplane
- buy a PCIE SAS HBA with staggered spinup support
- wire the proprietary connector head up to a 12V and 20A(multiplied by the number of 8 drive R720 backplanes you have) PSU 
- profit

## links
---
