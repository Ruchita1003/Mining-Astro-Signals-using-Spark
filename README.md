# Mining-Astro-Signals-using-Spark

## This project was executed on [Bridges-2](https://www.psc.edu/resources/bridges-2/), [Pittsburgh Super Computing Centre's](https://www.psc.edu/) flagship super computer.

A pdf of the code and its corresponding output can be found [here!](https://github.com/Ruchita1003/Mining-Astro-Signals-using-Spark/blob/main/Mining_Astro_Signals_using_Spark.pdf).

### A peek into the data:
The data on Bridges-2 consisted of a series of signals stores as:<br>
_ascension (degrees),  declination (degrees),  time (seconds),  frequency (MHz)_
    
Ascension and Declination denote the location of the astronomical object. Time refers to the time in seconds recorded after a point in time t. Frequency is the radiofrequency of the signals emitted by the astronomical objects.

These are radiofrequency signals captured by an array of instruments scanning a solid angle of the sky.

The data is almost like all real data, a little noisy and has sources of errors. In our case the angular coordinates have 0.1 degrees error, the signal frequency has 0.1 MHz error and the timebase/period error is <0.1s (i.e. 1 standard deviation).

### Goal:
Our goal is to find the most regular temporarily repeating RF source.

Our target will be found in the same location (within error) of the sky, on the same frequency (within error) chirping for the most blips, regularly spaced in time during that active period. So.....

..........blip...........blip............blip...............blip..................blip.........................

Again, we are looking for the most blips!

### Execution:

The steps mentioned below should be followed before executing the code in the aforementioned pdf:
1) Log into Bridges-2 via the terminal.
2) cp the datafile to where you want to work with you PySpark Session.
3) get an interactive node
4) load the spark module
5) start a pyspark session
6) load a datafile and start exploring the space! :satellite::telescope::stars: (Refer to the pdf from here on)

### Conclusion:

In my opinion the most regular temporarily repeating RF is located around ascension 73 degrees, declination 100 degrees and has a frequency of around 6970 Mhz. This target is found in the same location, on the same frequency (all within errors) emitting the most blips regularly spaced in time after about every 4 seconds during that active period.
