# 0219-CX4L-015-IC
Identification of mysterious IC from car redio.

The marking is:

0219
CX4L
 015
 
![IMG_20250427_172437](https://github.com/user-attachments/assets/83a8edaf-0b45-483c-9d4a-86bd38e0d0be)

TL;DR: It is Si4702 or Si4703.

I got it from some random car radio PCB and was curious if i could reuse in radio.
After some googling i found absolutly no info on what this IC could be (and that's the reason this repo exists).
From the begining i was thinking that its from skyworks, Si47xx series, because they are the most common in modernish car radios.  luckily the datasheet are available for the whole series, so i started comparing pins that are easy to identify on the circuit board (like power, ground, antenna etc.) with the pinout from datasheet. The good news is they matched, the bad news the pinouts are almost identical for Si740x ICs and Si743x ICs but they are very different function wise.
So i decided to brute force it by connecting them to Arduino nano and trying to communicate with the ic using i2c and PU2CLR Si4735 or PU2CLR Si470X library. First one could not find the ic, but the second one worked! So it's likely Si4702 or Si4703

Sensitivity wise the IC not great, but also not terrible, fine for city radio.

That's the fragment of the PCB:

![IMG_20250427_172451](https://github.com/user-attachments/assets/57924b14-6c0c-4fc1-980c-8b0c1acc7e05)
![IMG_20250427_172503](https://github.com/user-attachments/assets/6328d395-121a-48d5-a918-e2dc56214164)

And pinout of the pads:

![IMG_20250427_180453](https://github.com/user-attachments/assets/762abf54-5d27-4773-b278-d37e0a7633d5)
