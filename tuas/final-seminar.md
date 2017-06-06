---
title: "Spectrum monitoring application implementation using software-defined radio"
author: "Jarmo Kivekäs"
subtitle: Commissioned by TUAS radio lab

date: 6.6.2017
toc: true
---


# Thesis Topics


- Applications of Spectrum Monitoring
- Spectrum Sensing Methods
- Software Defined Radio
- System implementation
- Test and measurements

---

![Ettus Research USRP n210](n210.jpg)

---

# Tools & Practicalities

- USRP (Ettus Research/National Instruments)
- GNU Radio
- python (numpy, pandas, matplotlib)
- Jupyter notebooks
    - plenty of detailed notes
    - annotate all the data
- Julia
- Baudline



# Tools & Practicalities

- Started work late December 2016
- Topic not strictly specified
    - Articles from IEEExplore
    - Annotate and save reference material
- Kept all personal deadlines
    - there weren't any other
- Writing and practical work complete


- BibTeX, Git, Rsync, Makefiles
- Lab notebooks

---


![System control flow overview](../doc/img/control-flow.png)

---

![Sample rates chosen to maximize (20 MSPS) and minimize (25 MSPS) the effect of CIC roll-off\label{fig:cic-rolloff}](../doc/img/cic-rollof-by-sample-rate-superpose.png){ width=100% }

---

![Baudline used to distinguish between 50 Hz peaks (left). Comparisons done with an FSH4 spectrum analyzer (right).\label{fig:baud50}](../doc/img/50-hz-combined.png){ width=100% }

---

<!-- ![The level of the noise floor can be lowered by increasing the number of FFT bins\label{fig:noise-vs-bins}](../doc/img/noise-vs-bins.png){ width=100% }

--- -->

![The edge of a high-throughput digital signal without downtime\label{fig:hist-DVB}](../doc/img/histogram-DVB.png){ width=100% }

---

![A mobile communications band not in use 100% of the time\label{fig:hist-mobile}](../doc/img/histogram-mobile.png){ width=100% }

---

![Time-average of the measurements shown as a histogram in figure \ref{fig:hist-mobile}\label{fig:avg-mobile}](../doc/img/mobile-average-spectrum.png){ width=100% }

---

![225 MHz span of spectum stiched from multiple measurements. \label{fig:hist-long}](../doc/img/stiched-spectum-0-2.png){ width=100% }

---

<!-- ![Mechanisms for DC-offset: A) LO leakage, B) LO re-radiation, C) in-band interference\label{fig:dc-offset}](../doc/img/dc-offset.png)

--- -->

![DC-offset can cause sever data quality issues.\label{fig:dc-offset-issues}](../doc/img/dc-offset-impact.png){ width=100% }

---


# Conclusion


- Fun, interesting and rewarding
- Great tools and workflows
- Very independent work
- Still have some ideas...
- Overall a success
