# Dataset
:smile: Paper: Data-Model Dual-Driven for Spectrum Prediction: A Deep Learning with Bayesian Theory Approach
----
__1. Introduction__

This dataset is used to validate the algorithm proposed in this work. Figure 1 shows the real platform where the simulated communication is interfered.

.<div align=center><img src="https://github.com/pgl1234/spectrum-data/blob/main/Images/platform.png" width="650" height="430" /></div>
<p align="center">  
 Figure 1. Real simulation experiment platform.
</p>

We simulate a MU to interfere with the wireless communication link. The jammer uses USRP 2943R. Multiple interference modes are adopted (e.g., sweep interference, fixed frequency interference, etc.), the interference to signal ratio is 10 dB, and interference power is greater than -50 dBm. Spectrum sensor monitoring range is 50 MHz to 2.2 GHz. Transmitter and receiver operating power is less than -50 dBm. <br>

The spectrum analyzer is used to collect spectrum data. Herein, either interfering H2B or interfering H2H is considered interfering. Due to the laboratory scenario, the distance between the jammer antenna and the user antenna is relatively close, so channel fading is not considered. The HU nodes are assumed to communicate between 1300 MHz and 1700 MHz, and every 20 MHz is divided into a communication channel, a total of 20 channels. 20-time slots are an interference period. The power is collected every 0.1 seconds. If the measured power exceeds -50 dBm, the channel cannot be communicated at the current time. During this experiment, a channel power sequence of 4000-time slots is generated. 

__2. Load Dataset__

File Org_Sensing_Spectrum_Dataset.txt is the dataset.

__2. The Proposed Method__

.<div align=center><img src="https://github.com/pgl1234/spectrum-data/blob/main/Images/Method_frame.png" width="800" height="300" /></div>
<p align="center">  
 Figure 2. Structure of the proposed method.
</p>

In this paper, we have proposed a DL-BO method for spectrum prediction. Specifically, a communication link interference scenario is considered to model the spectrum prediction problem. Then, we design a prediction model composed of stacked Bi-LSTM, which can accurately capture the temporal correlation of spectrum data. Based on model-driven, we design a Bayesian regression method to optimize the hyperparameters of the model, achieving a global optimum in a given hyperparameter space. On a real experimental platform, simulation results have shown that the proposed prediction method dramatically outperforms different benchmarks under different parameter settings.


