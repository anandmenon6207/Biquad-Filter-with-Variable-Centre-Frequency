*BandPass using LCR Circuit* 
- I have made this just to understand the workings of cascading a low pass and high pass filter
<img width="645" height="313" alt="image" src="https://github.com/user-attachments/assets/bc7abdb4-c4db-44ef-8552-046afe214159" />

- **OUTPUT** - A very shabby band pass voltage found between R2 and C2
- **Learnings:** A band pass filter can be built by cascading a high pass stage (C1, R1) and a low pass stage (R2, C2). The high pass corner (~10.6 kHz) sets the lower edge of the band and the low pass corner (~106 kHz) sets the upper edge.
- The output was a broad, low-Q hill with a peak gain of about -6.5 dB, not a sharp peak at 0 dB.
- The two stages load each other, since the second stage draws current from the first, and a passive RC network can only attenuate, never amplify. Buffering the stages with op-amps would remove the loading.
- Getting a sharp, tunable response needs an active, resonant design, which is why I moved to the Tow-Thomas biquad.
  
<img width="959" height="479" alt="image" src="https://github.com/user-attachments/assets/fd35c7b3-2767-44cd-af27-2bc6f2963163" />
