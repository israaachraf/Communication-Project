# Communication-Project

# General Instructions in all schemas:
#### 1. Random Integer Generator
* Initial seed = 37
* Sample time = 0.1s
* Samples per frame = 100
#### 2. AWGN Channel
* Initial seed = 67
* Number of bits per symbol = 1
* Input signal power = 1
* Symbol period = 1s
* Simulation time = 1000s
#### 3.BER diagrams are set from -10 to 10 dB
------------------------------------------------------------------
# Binary Phase Shift Keying Modulation
#### This model simulates binary phase shift keying modulation (BPSK), which is a method for converting a digital signal to a complex signal. In this technique, the sine wave carrier takes two phase reversals such as 0° and 180°. BPSK is basically a Double Side Band Suppressed Carrier (DSBSC) modulation scheme, for message being the digital information.
### The modulation Schema contains: 
1.	The Random Integer Generator block, block generates uniformly distributed random integers in the range [0, M-1], where M is specified by the Set size parameter
2.	The BPSK Modulator Baseband block, to the right of the Integer Random Generator block, modulates the signal.
3. The Constellation Diagram block, displays a scatter plot of the signal without the added noise.
4.	The AWGN Channel block models a noisy channel by adding white Gaussian noise to the modulated signal.
5.	The Constellation Diagram block, displays a scatter plot of the signal with added noise.
6.	The BPSK Demodulator Baseband block Baseband block, to the right of the AGWN channel demodulates the signal.
7.	The Error Rate Calculation block counts symbols that differ between the received signal and the transmitted signal.
8.	The To Workspace block, labeled Ber outputs the results to the workspace to use when plotting results.
## The Modulation Schema
![BPSK](/BPSK/BPSK.png)
## Instruction SET:
* Random Generator set size = 2
## Scatter Plot:
![BPSK Before Noise](/BPSK/Scatter_Plot_Before_Noise.png)
![BPSK After Noise](/BPSK/Scatter_Plot_After_Noise.png)

## BER performance figure:
![Error Curve](/BPSK/Error_Curve_bpsk.png)



------------------------------------------------------
# Quadrature Phase Shift keying Modulation
#### This model simulates quadrature amplitude modulation (QPSK), which is a method for converting a digital signal to a complex signal. In this technique the sine wave carrier takes four phase reversals such as 0°, 90°, 180°, and 270°.
### The modulation Schema contains: 
1.	The Random Integer Generator block, block generates uniformly distributed random integers in the range [0, M-1], where M is specified by the Set size parameter
2.	The QPSK Modulator Baseband block, to the right of the Integer Random Generator block, modulates the signal.
3. The Constellation Diagram block, displays a scatter plot of the signal without the added noise.
4.	The AWGN Channel block models a noisy channel by adding white Gaussian noise to the modulated signal.
5.	The Constellation Diagram block, displays a scatter plot of the signal with added noise.
6.	The QBSK Demodulator Baseband block Baseband block, to the right of the AGWN channel demodulates the signal.
7.	The Error Rate Calculation block counts symbols that differ between the received signal and the transmitted signal.
## The Modulation Schema
![QPSK](/QPSK/QPSK.png)
8.	The To Workspace block, labeled Ber outputs the results to the workspace to use when plotting results.
## Instruction SET:
* Random Integer Generator set size = 4
## Scatter Plot:
![QPSK Before Noise](/QPSK/Scatter_Plot_Before_Noise_qpsk.png)
![QPSK After Noise](/QPSK/Scatter_Plot_After_Noise_qpsk.png)

## BER performance figure:
![Error Curve](/QPSK/Error_Curve_qpsk.png)
------------------------------------------------------
# Frequency Shift Keying Modulation
#### This model simulates frequency shift keying modulation (FSK), which is a method for converting a digital signal to a complex signal. In this techinque the frequency of the carrier signal varies according to the digital signal changes.
### The modulation Schema contains: 
1.	The Random Integer Generator block, block generates uniformly distributed random integers in the range [0, M-1], where M is specified by the Set size parameter
2.	The FSK Modulator Baseband block, to the right of the Integer Random Generator block, modulates the signal.
3. The Constellation Diagram block, displays a scatter plot of the signal without the added noise.
4.	The AWGN Channel block models a noisy channel by adding white Gaussian noise to the modulated signal.
5.	The Constellation Diagram block, displays a scatter plot of the signal with added noise.
6.	The FSK Demodulator Baseband block, to the right of the AGWN channel demodulates the signal.
7.	The Error Rate Calculation block counts symbols that differ between the received signal and the transmitted signal.
8.	The To Workspace block, labeled Ber outputs the results to the workspace to use when plotting results.
## The Modulation Schema
![FSK](/FSK/FSK.png)
## Instruction SET:
* Random Integer Generator set size = 8
## Scatter Plot:
![FSK Before Noise](/FSK/Scatter_Plot_Before_Noise_fsk.png)
![FSK After Noise](/FSK/Scatter_Plot_After_Noise_fsk.png)

## BER performance figure:
![Error Curve](/FSK/Error_Curve_fsk.png)

------------------------------------------------------

# 16-Quadrature Amplitude Modulation
#### This model simulates quadrature amplitude modulation (QAM), which is a method for converting a digital signal to a complex signal. The model modulates the signal onto a sequence of complex numbers that lie on a lattice of points in the complex plane, called the constellation of the signal.

1.	The Random Integer Generator block, block generates uniformly distributed random integers in the range [0, M-1], where M is specified by the Set size parameter
2.	The Rectangular QAM Modulator Baseband block, to the right of the Integer Random Generator block, modulates the signal using baseband 16 QAM.
3. The Constellation Diagram block, displays a scatter plot of the signal without the added noise.
4.	The AWGN Channel block models a noisy channel by adding white Gaussian noise to the modulated signal.
5.	The Constellation Diagram block, displays a scatter plot of the signal with added noise.
6.	The Rectangular QAM Demodulator Baseband block, to the right of the AGWN channel demodulates the signal.
7.	The Error Rate Calculation block counts symbols that differ between the received signal and the transmitted signal.
8.	The To Workspace block, labeled Ber outputs the results to the workspace to use when plotting results.
## The Modulation Schema
![QAM16 ](/QAM16/QAM16.png)
## Instruction SET:
* Random Integer Generator set size = 16

* Modulator and demodulation: Normalization method = Average power
## Scatter Plot:
![QAM16 Before Noise](/QAM16/Scatter_Plot_Before_Noise_qam16.png)
![QAM16 After Noise](/QAM16/Scatter_Plot_After_Noise_qam16.png)

## BER performance figure:
![Error Curve](/QAM16/Error_Curve_qam16.png)

-----------------------------------------------------------
# 64-Quadrature Amplitude Modulation
#### This model simulates quadrature amplitude modulation (QAM), which is a method for converting a digital signal to a complex signal. The model modulates the signal onto a sequence of complex numbers that lie on a lattice of points in the complex plane, called the constellation of the signal.

1.	The Random Integer Generator block, block generates uniformly distributed random integers in the range [0, M-1], where M is specified by the Set size parameter
2.	The Rectangular QAM Modulator Baseband block, to the right of the Integer Random Generator block, modulates the signal using baseband 64 QAM.
3. The Constellation Diagram block, displays a scatter plot of the signal without the added noise.
4.	The AWGN Channel block models a noisy channel by adding white Gaussian noise to the modulated signal.
5.	The Constellation Diagram block, displays a scatter plot of the signal with added noise.
6.	The Rectangular QAM Demodulator Baseband block, to the right of the AGWN channel demodulates the signal.
7.	The Error Rate Calculation block counts symbols that differ between the received signal and the transmitted signal.
8.	The To Workspace block, labeled Ber outputs the results to the workspace to use when plotting results.
## The Modulation Schema
![QAM64](/QAM64/QAM64.png)
## Instruction SET:
* Random Integer Generator set size = 64

* Modulator and demodulation

Normalization method = Average power
## Scatter Plot:
![QAM64 Before Noise](/QAM64/Scatter_Plot_Before_Noise_qam64.png)
![QAM64 After Noise](/QAM64/Scatter_Plot_After_Noise_qam64.png)

## BER performance figure:
![Error Curve](/QAM64/Error_Curve_qam64.png)

-----------------------------------------------------------------------

# After adding raised cosine 
#### The Raised Cosine Transmit Filter and Raised Cosine Receive Filter blocks are designed for raised cosine filtering. Each block can apply a square-root raised cosine filter or a normal raised cosine filter to a signal. You can vary the rolloff factor and span of the filter.
#### The Raised Cosine Transmit Filter and Raised Cosine Receive Filter blocks are tailored for use at the transmitter and receiver, respectively. The transmit filter outputs an upsampled (interpolated) signal, while the receive filter expects its input signal to be upsampled. The receive filter lets you choose whether to have the block downsample (decimate) the filtered signal before sending it to the output port.
#### Both raised cosine filter blocks introduce a propagation delay.
--------------------------------------------------------------
# BPSK
## The Modulation Schema:
![BPSK](/raisedcos_code_screen/bpsk_cosine.png)
## The Change in the instruction Set for Binary Phase Shift Keying Modulation :
* Raised Cosine Filter Transmitter : Filter span in symbols = 8
* Raised Cosine Filter Reciever : Filter span in symbols = 8
* Error Rate calculation : Recieve Delay = 8

## Scatter Plot for Binary Phase Shift Keying Modulation:
![Before](/raised_cosine_fig/Scatter_Plot_Before_Noise_bpsk_raised_cosine.png)
![After](/raised_cosine_fig/Scatter_Plot_After_Noise_bpsk_raised_cosine.png)
## BER performance figure for Binary Phase Shift Keying Modulation:
![After](/raised_cosine_fig/Error_Curve_bpsk_raised_cosine.png)
--------------------------------------------------------------
## QPSK
## The Modulation Schema:
![BPSK](/raisedcos_code_screen/qpsk_cosine.png)
## The Change in the instruction Set for Quadrature Shift Keying Modulation :
* Raised Cosine Filter Transmitter : Filter span in symbols = 8
* Raised Cosine Filter Reciever : Filter span in symbols = 8
* Error Rate calculation : Recieve Delay = 8
## Scatter Plot Set for Quadrature Shift Keying Modulation:
![Before](/raised_cosine_fig/Scatter_Plot_Before_Noise_qpsk_raised_cosine.png)
![After](/raised_cosine_fig/Scatter_Plot_After_Noise_qpsk_raised_cos.png)
## BER performance figure Set for Quadrature Shift Keying Modulation:
![After](/raised_cosine_fig/Error_Curve_qpsk_raised_cosine.png)
-----------------------------------------------------------
## FSK
## The Modulation Schema:
![BPSK](/raisedcos_code_screen/fsk_cosine.png)
* Raised Cosine Filter Transmitter : Filter span in symbols = 8
* Raised Cosine Filter Reciever : Filter span in symbols = 8
* Error Rate calculation : Recieve Delay = 8

## Scatter Plot for Frequency Shift Keying Modulation:
![Before](/raised_cosine_fig/Scatter_Plot_Before_Noise_fsk_raised_cos.png)
![After](/raised_cosine_fig/Scatter_Plot_After_Noise_qpsk_raised_cos.png)
## BER performance figure for Frequency Shift Keying Modulation:
![After](/raised_cosine_fig/Error_Curve_fsk_raised_cosine.png)
---------------------------------------------------------------
# 16-QAM
## The Modulation Schema
![BPSK](/raisedcos_code_screen/qam16_cosine.png)
## The Change in the instruction Set for 16-Quadrature Amplitude Modulation :
* Raised Cosine Filter Transmitter : Filter span in symbols = 8
* Raised Cosine Filter Reciever : Filter span in symbols = 8
* Error Rate calculation : Recieve Delay = 8


## Scatter Plot  for 16-Quadrature Amplitude Modulation:
![Before](/raised_cosine_fig/Scatter_Plot_Before_Noise_qam16_raised_cosine.png)
![After](/raised_cosine_fig/Scatter_Plot_After_Noise_qam16_raised_cos.png)
## BER performance figure  for 16-Quadrature Amplitude Modulation:
![After](/raised_cosine_fig/Error_Curve_qam16_raised_cosine.png)
---------------------------------------------------------------
## 64-QAM
## The Modulation Schema:
![BPSK](/raisedcos_code_screen/qam64_cosine.png)
## The Change in the instruction Set for 64-Quadrature Amplitude Modulation :
* Raised Cosine Filter Transmitter : Filter span in symbols = 8
* Raised Cosine Filter Reciever : Filter span in symbols = 8
* Error Rate calculation : Recieve Delay = 8
* QAM64 Modulator : Constellation ordering = Binary
* QAM64 Demodulator : Constellation ordering = Binary


## Scatter Plot  for 64-Quadrature Amplitude Modulation:
![Before](/raised_cosine_fig/Scatter_Plot_Before_Noise_qam64_raised_cos.png)
![After](/raised_cosine_fig/Scatter_Plot_After_Noise_qam64_raised_cos.png)
## BER performance figure  for 64-Quadrature Amplitude Modulation:
![After](/raised_cosine_fig/Error_Curve_qam64_raised_cosine.png)

