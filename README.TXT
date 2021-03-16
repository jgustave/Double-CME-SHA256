
I'm going to try and implement this design for my first FPGA work (and optimisticly my first ASIC work)

First thing I notice, Why not get rid of SHA-256(1)? Do it in software. Save a few gates there. 
Second Idea is that I would add a little bit of searching on the timestamp field. You could easily fit another 8 bits (256 seconds) of search space. 

![](https://github.com/jgustave/Double-CME-SHA256/blob/jd/overview1.jpg)


