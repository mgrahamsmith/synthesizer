================================================================================
TODO
================================================================================


Future Implementations
--------------------------------------------------------------------------------


Guitar String simulation
^^^^^^^^^^^^^^^^^^^^^^^^

* *Guitar string simulation pseudo-code:*
* sampleRate
* each sample, send speaker a number representing diaphram position.
* For every string that was plucked, create a ring buffer.
* Ring buffer:
    * When you get to the end of the array, jump back to the beginning.
* Every time you pluck a string, it creates a new ring buffer and sets it to whatever lenght needed for the note being plucked.
* Go through each element of ring buffer once per sample.
* ringBuf[200] is filled with random values between 1 and -1.
* output 1 element of ringBuf per sample.
* Every 200 samples it repeats.
* For A, make the note long enough to repeat every 440 seconds.
* Determined by the sample rate.
* Go back and mulitply every ringBuf element by 0.9 and it will fade to 0 after enough iterations.
