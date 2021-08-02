# Journal of 2-day Training Workshop on IC Design of Phase-Locked Loop (PLL) using Google SkyWater 130nm

![2-day Training Workshop on IC Design of Phase-Locked Loop (PLL) using Google SkyWater 130nm](PLL_VSD_ad.png)

The Phase-Locked Loop (PLL) is one of the most essential analog block in any integrated circuit circuit employing a (reasonably) high frequency clock signal such as a microprocessor. On-chip oscillators such as ring oscillators built by connecting an odd number of inverters in series and in feedback does provide a clock signal of frequency 1/(2*n*d), where n is the number (odd) of inverters in the ring and d is the delay of each inverter. However such a clock signal has too much phase noise or jitter and is almost unusable for high speed synchronous digital design. On the other hand, crystal oscillators have extemely high spectral purity i.e., low phase noise but they are available only to generate a specific set of frequencies such as 32 kHz, 383 kHz etc. which have specific applications. However, we would like to be able to generate a clock signal of arbitrary frequency but with a spectral purity comparable to that of a crystal oscillator. The PLL comes in this context. The PLL is essentially a feedback control system which dynamically adjusts the phase of the on-chip oscillator (typically a voltage controlled ring oscillator) by comparing its output with a reference signal typically the crystal oscillator. Since the I/O pads of an IC typically has very large capacitance, the frequency of the crystal oscillator connected to the input of the IC has a small frequency while the output of the PLL will be a multiple of the input crystal frequency. This 'frequency multiplication' is achieved by employing a frequency divider in the feedback path of the PLL.

## Block Diagram of PLL

![PLL Block Diagram](PLL_blk.png)

The block diagram of the PLL shown above consists of a 
