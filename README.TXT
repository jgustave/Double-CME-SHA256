
I'm going to try and implement this design for my first FPGA work (and optimisticly my first ASIC work)

First thing I notice, Why not get rid of SHA-256(1)? Do it in software. Save a few gates there. 
Second Idea is that I would add a little bit of searching on the timestamp field. You could easily fit another 8 bits (256 seconds) of search space. 

A timestamp is accepted as valid if it is greater than the median timestamp of previous 11 blocks, and less than the network-adjusted time + 2 hours. "Network-adjusted time" is the median of the timestamps returned by all nodes connected to you. As a result block timestamps are not exactly accurate, and they do not need to be. Block times are accurate only to within an hour or two.


![](https://github.com/jgustave/Double-CME-SHA256/blob/jd/overview1.jpg)


