# 866 MHz PN-Sequence Assisted FMCW-GPR Based Buried Object Detection



## 1. Project Overview

Ground-Penetrating Radar (GPR) is a non-destructive sensing technology used to investigate subsurface structures by transmitting electromagnetic signals into the ground and analyzing the reflected signals.

This project focuses on the development and experimental evaluation of an **866 MHz PN-Sequence Assisted Frequency-Modulated Continuous-Wave Ground-Penetrating Radar (FMCW-GPR)** system for buried-object detection.

The system investigates RF signal generation, transmission and reception, beat-frequency extraction, analog-to-digital conversion, and digital signal processing. The objective is to study how reflected radar signals can be analyzed to distinguish potential buried targets from soil-related responses and system noise.

The project also explores the influence of soil properties and moisture content on radar measurements, with the long-term goal of developing an intelligent, soil-adaptive buried-object detection system suitable for robotic ground scanning.

## 2. Project Objectives

- Develop and test an 866 MHz FMCW-GPR hardware platform.
- Investigate PN-sequence-assisted signal generation or processing.
- Study RF transmission, reception, mixing, and beat-signal extraction.
- Acquire radar signals for digital processing and visualization.
- Analyze frequency-domain characteristics using Fast Fourier Transform (FFT).
- Investigate the effects of soil type, moisture, and target material on radar responses.
- Document hardware implementation and experimentally observed results.
- Explore automated buried-object detection and classification.

## 3. Key Features

- 866 MHz RF hardware implementation.
- FMCW radar signal processing.
- PN-sequence-assisted radar architecture.
- Beat-frequency analysis and FFT visualization.
- Hardware testing and experimental documentation.
- Investigation of soil-dependent radar responses.
- Potential integration with a mobile robotic platform.

*Feature status should be updated as each function is implemented and verified.*

## 4. System Architecture

The proposed system follows this general signal-processing chain:

RF Signal Generation → Frequency Sweep → Transmit Antenna → Subsurface Interaction → Receive Antenna → RF Mixing → Beat Signal → ADC Acquisition → Digital Signal Processing → Target Detection Analysis

### 4.1 RF Signal Generation

The RF subsystem generates the radar signal around the 866 MHz operating frequency. The FMCW waveform provides frequency variation over time, while the PN-sequence-assisted circuitry is investigated as part of the signal-generation or processing architecture.

The exact sweep bandwidth, chirp duration, and PN-sequence configuration depend on the implemented hardware.

### 4.2 Transmission and Reception

The transmit antenna radiates electromagnetic energy toward the ground. Reflections may occur at boundaries between materials with different electromagnetic properties.

The receive antenna captures the returned signal for further processing. The received signal depends on target properties, depth, soil composition, moisture, antenna coupling, and system noise.

### 4.3 Beat-Signal Generation

The received signal is combined with a reference or transmitted signal using a mixer. The resulting beat signal contains frequency components related to the transmitted waveform and the reflected signal's delay.

For an ideal linear FMCW chirp, the approximate relationship is:



where (v) is the electromagnetic wave propagation velocity in the soil.

The actual relationship depends on the waveform, propagation medium, system calibration, and processing method.

## 5. Hardware Components

The hardware used or investigated in this project includes:

| Subsystem                                         | Purpose                                       |
| ------------------------------------------------- | --------------------------------------------- |
| 866 MHz RF hardware                               | Radar signal generation and reception         |
| PN-sequence circuitry                             | Sequence generation or related signal control |
| Transmit antenna                                  | Radiates radar energy toward the ground       |
| Receive antenna                                   | Captures reflected electromagnetic signals    |
| RF mixer                                          | Produces the beat signal                      |
| Analog signal conditioning                        | Prepares the signal for digitization          |
| ADC and acquisition interface                     | Samples the beat signal                       |
| Raspberry Pi or microcontroller, where applicable | Acquisition control and data processing       |
| Power supply                                      | Provides the required electrical power        |

The exact component models, operating voltages, and interconnections should be documented using the actual hardware configuration.

## 6. Software and Development Tools

Tools used in the project may include:

- Arduino IDE for embedded firmware, where applicable.
- Python for signal analysis and visualization, where applicable.
- MATLAB and Simulink for signal-processing models, where applicable.
- LTspice for circuit simulation, where applicable.
- GitHub for source control and technical documentation.

Only list tools actually used in the project.

## 7. Signal Processing Methodology

The radar signal-processing workflow may include the following stages:

1. **Data acquisition:** Capture digitized beat-signal samples.
2. **Preprocessing:** Remove unwanted offsets and prepare the data for analysis.
3. **Windowing:** Apply an appropriate window function to reduce spectral leakage.
4. **FFT analysis:** Transform time-domain samples into the frequency domain.
5. **Noise analysis:** Investigate unwanted spectral components and environmental interference.
6. **Feature extraction:** Identify relevant peaks, amplitudes, frequency characteristics, and repeatability.
7. **Target evaluation:** Compare measurements obtained with and without a buried target.
8. **Soil-adaptive analysis:** Investigate whether soil type and moisture measurements can help interpret radar responses.

The final implementation and detection criteria should be documented after validation.

## 8. Experimental Setup

Experiments should document the following parameters whenever available:

- Operating frequency and RF sweep bandwidth.
- Chirp duration and sweep configuration.
- Antenna type, orientation, and spacing.
- ADC model, sampling frequency, and resolution.
- Soil type and moisture condition.
- Buried-object material, dimensions, and depth.
- Distance between the antenna and ground surface.
- Measurement duration and repeatability.
- Environmental and calibration conditions.

Controlled experiments are important for distinguishing actual target responses from antenna coupling, surface reflections, and other sources of interference.

## 9. Experimental Results

This section contains photographs of the implemented hardware, measurement setups, acquired waveforms, frequency spectra, and documented test results.

### Hardware Implementation

Add photographs showing the RF circuitry, antennas, signal-generation circuitry, and complete hardware setup.

### Signal Analysis

Include measured time-domain waveforms and FFT plots, together with the acquisition settings and observations.

### Buried-Object Testing

Document the target material, depth, soil condition, and corresponding radar measurements for each test.

### Results Summary

Summarize the observed signal characteristics, repeatability, noise sources, limitations, and conditions under which detection was successful.



## 11. Applications

Potential application areas include:

- Buried-object detection research.
- Subsurface inspection and material characterization.
- Underground utility detection research.
- Robotic ground-scanning systems.
- Experimental studies of radar responses in different soils.

Detection of hazardous objects requires separate validation and should not be assumed from successful detection of ordinary test objects.

## 12. Current Development Status

Update this section to reflect the actual status of the project.

- [ ] RF signal generation and sweep verification.
- [ ] PN-sequence-assisted subsystem verification.
- [ ] Transmit and receive chain characterization.
- [ ] Beat-signal acquisition.
- [ ] ADC integration and sampling verification.
- [ ] FFT-based signal analysis.
- [ ] Controlled buried-object experiments.
- [ ] Soil-type and moisture comparison.
- [ ] Automated target detection and classification.
- [ ] Robotic platform integration.

## 13. Challenges and Limitations

Potential engineering challenges include:

- Soil-dependent attenuation and dielectric properties.
- Antenna coupling and surface reflections.
- Noise and unwanted frequency components.
- ADC sampling limitations and analog bandwidth.
- Calibration of beat frequency against target depth.
- Repeatability across different soil and target conditions.

These challenges should be discussed alongside the observations from actual experiments.

## 14. Future Improvements

- Improve RF isolation and receiver sensitivity.
- Optimize analog signal conditioning and noise reduction.
- Develop reliable ADC acquisition and data-transfer software.
- Automate FFT analysis and target-response visualization.
- Investigate soil-adaptive signal-processing techniques.
- Evaluate machine-learning methods using experimentally collected data.
- Integrate the GPR module with a robotic ground-scanning rover.

## 15. Research and Learning Outcomes

This project provides practical experience in RF electronics, FMCW radar principles, antenna systems, embedded acquisition, digital signal processing, experimental characterization, and subsurface sensing.

## 16. Author

**Sanath**

Project: 866 MHz PN-Sequence Assisted FMCW-GPR Based Buried Object Detection

## 17. Disclaimer

This repository documents an engineering research and development project. Performance claims are limited to the hardware configuration and experiments that have been verified. The system should not be treated as a certified safety device or as proof of reliable landmine or unexploded-ordnance detection.
