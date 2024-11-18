java c
Multi-Channel Communications
Mini-Project #3 Diversity
Due October 16, 2024
1 Mini-Project Overview
In this third project you are going to implement a simple transmitter and receiver in complex baseband that incorporate diversity techniques and channel estimation using pilot symbols.You will turn in two primary components: (1) Matlab code (uploaded to Canvas as a zip file) and (2) A report validating your design (uploaded to Canvas as a pdf file and a hard copy submitted in class).
2 Detailed Description
You will create a Matlab function titled transmit.m which accepts as its input an Nb × 1 vector b where Nb is the number of bits to be transmitted in a specific packet (including pilots). The function outputs a matrix X of transmitted samples that is k/Nb × Nt matrix where k is the number of bits per symbol for the chosen modulation scheme. Again, the transmit symbols are in complex baseband. You should also in some way include input parameters to control the chosen modulation scheme and other transmit parameters (e.g., number and location of pilot symbols). The modulation schemes are ultimately up to you, but should be PSK and/or QAM. I recommend incorporating BPSK, QPSK and 16-QAM. Note that you cannot use built-in Matlab functions. You may use such functions as guidance, but ultimately you should write your own code and it should be self-contained. You must also create a function titled receive.m which accepts a Mr × k/Nb matrix of corrupted complex samples (one sample per symbol) and outputs a Nb×1 vector ˆb of bit estimates. Note that we are not going to worry about pulse-shaping at this point. We will incorporate OFDM later in the class.
3 Required Validation
You will create a report describing your functions briefly and providing validation plots. Specif-ically, you must validate the modulator and demodulator functions by providing the following plots/analyses:
1. AWGN
(a) Plot the simulated performance of each modulation scheme along with the theoretical performance in an AWGN channel. Please use a semilogy plot with BER on the y-axis ranging from 10−5to 1 and Eb/No on the x-axis ranging from 0-10dB. You will need to create a new function AWGN.m which takes the received samples on each antenna and the SNR as inputs and outputs the received samples with additive noise. You can assume perfect channel knowledge for AWGN.
2. Fading Channels Part I - Receive Diversity
Unless otherwise stated, please assume that the correlation between the channels observed on each antenna is approximately zero. You can代 写Multi-Channel Communications Mini-Project #3 DiversityMatlab
代做程序编程语言 do this by generating independent channels or by using your previously created channel model with appropriately chosen antenna spacing and angle spread. Assume that the fading is slow (much slower than the symbol duration). You can do this by choosing appropriate values for the symbol rate and fading rate (e..g, 1Msps symbol rate and 50Hz maximum Doppler). For the simulations, you must use pilot symbols to estimate the channel.
(a) Derive the performance of L-branch MRC with BPSK in Nakagami fading. Show that when m = 1 the expression simplifies to the performance in Rayleigh fading.
(b) Plot the simulated performance of each modulation scheme when there is a single trans-mit antenna and Mr = 1, 2, 4 receive antennas (use maximal ratio combining) in Rayleigh fading. Please use a semilogy plot with BER on the y-axis ranging from 10−5 to 1 and γb = Eb/No on the x-axis ranging from 0-20dB. Vary the number of pilots to find a good trade-off between performance and efficiency.
(c) Compare the above simulated performance with theoretical performance. Assume per-fect channel estimation for the theoretical performance.
(d) Repeat (2b) and (2c) for Mr = 2 with a channel correlation of 0.8 between receive antennas.
(e) Repeat (2b) and (2c) for Mr = 2 with Nakagami fading (m = 1, 4).
3. Fading Channels Part II - Transmit Diversity
Unless otherwise stated, please assume that the correlation between the channels observed on each antenna is approximately zero. You can do this by generating independent channels or by using your previously created channel model with appropriately chosen antenna spacing and angle spread. Assume that the fading is slow (much slower than the symbol duration). For the simulations, you must use pilot symbols to estimate the channel.
(a) Simulate the performance space-time block coding (Alamouti code) with two transmit antennas and two receive antennas. Compare to theoretical performance.
(b) Simulate the performance of antenna selection at the transmitter (assuming perfect feedback) and MRC at the receiver for two transmit antennas and two receive antennas. Compare with theoretical performance. Also, simulate the impact of 10% error rate on the one-bit feedback.
(c) Simulate the performance of Maximal Ratio Transmission (assuming perfect feedback) for two transmit antennas and two receive antennas. Compare with theoretical perfor-mance.
(d) Compare the performance of the four transmit diversity schemes. What are the pros and cons of each?





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
