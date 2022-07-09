# Dataset
Paper: Deep Learning and Bayesian Optimization Based Spectrum Availability Prediction in Cognitive Radio Networks
----

This dataset is used to validate the algorithm proposed in this work. Figure 1 shows the real platform where the simulated communication is interfered.

![](https://github.com/pgl1234/spectrum-data/blob/main/Images/platform.png)
.<div align=center><img src="https://github.com/pgl1234/spectrum-data/blob/main/Images/platform.png" width="300" height="450" /></div>
<p align="center">  
 Figure 1. Real simulation experiment platform.
</p>

We simulate a malicious user to interfere the wireless communication link. The jammer uses USRP 2943R to achieve, multiple interference modes are adopted (e.g., sweep interference, fixed frequency interference, etc.), interference to signal ratio is 10 dB and interference power is greater than -50 dBm. Spectrum sensor monitoring range is 50 MHz to 2.2 GHz. Transmitter and receiver operating power is less than -50dbm. <br>

The spectrum analyzer is used to collect spectrum data. Herein, it is interfered whether the malicious user interferes honest users to base station (H2B) and honest users to honest users (H2H) communication. Due to the laboratory scenario, the distance between the jammer antenna and the user antenna is relatively close, so channel fading is not considered. The honest user nodes are assumed to communicate between 1300 MHz and 1700 MHz, and every 20 MHz is divided into a communication channel, a total of 20 channels. Every 20 time slots is an interference period. The power is collected every 0.1 seconds. If the measured power exceeds -50 dBm, the channel cannot be communicated at the current time. During this experiment, a channel power sequence of 4000 time slots is generated. 
