





# Introduction



# Background

## Spectrum Monitoring

Conventionally sections of radio spectrum are allocated for use in a
particular application, and the rights to transmit on those section
are licensed by a governing body. Licensees may obtain licenses for
comparatively long spans of time, during which the allocated spectrum
may not be used used continuously and in full. \cite{subramaniam15}

The Finnish Communications Regulatory Authority (FICORA) regulates the
use of frequencies 9 kHz -- 400 GHz \cite{ficoraReg15}.

Advances in radio technology allows the implementation of flexible
radio systems that reduce under utilization of available RF spectrum
\cite{gronroos16}.  Thanks to increased flexibility, transmission
frequencies, bandwidth, and modulation schemes can be changed rapidly
in a dynamic way in order to accommodate for changes in the available
spectrum.  Spectrum monitoring is a key technology when considering the
use of dynamic spectrum access \cite{zennaro12}.


<!--  read hoyhtya16 and wirte something in this section-->

## Applications of Spectrum Monitoring


### Opportunistic Spectrum access

A concrete example dynamic spectrum access is the secondary use of TV
whitespace (TVWS). In Finland

### Enforcement of Radio Regulation

## Licensed Shared Access

Licensed shared access (LSA) is an approach to radio spectrum regulation
that allows further use of spectrum that is previously allocated to
an incumbent user.  LSA is based on a framework where the incumbent
user, one or several LSA licensees -- i.e new users -- and the spectrum
regulation authority collectively agree on a sharing scheme. The sharing
scheme in LSA is controlled in a way that both the incumbent user, as
well as the licensee can expect predictable quality-of-service and are
protected from interference. \cite{lsa}

Availability information and spectrum access policies are held centrally
in an LSA repository.


## Spectrum Sensing Methods

TODO: Sensing applications can be either generalized, or designed for a
specific type of transmission, in order to monitor the use of particular
standardized channels of a radio system.

### Energy Detection

<!--  subramanima15 has many references to sensing studies --> <!-- "using
the energy detection method with fixed-threshold [9]" \cite{subramaniam15}
-->

Energy detection is commonly used in research applications to determine
the utilization of radio frequencies \cite{subramaniam15}.  In a
simplistic application energy detection can be done by digitizing a span
of spectrum using a software defined radio, or a purpose-built spectrum
analyzer.  A binary decision about whether a particular frequency is in
use is made by comparing the received RF energy on that frequency to a
fixed threshold value. \cite {subramaniam15}

Energy detection using a fixed threshold is problematic.  Threshold values
that are set manually are error prone, and may need re-adjustment
depending on the environment in which measurements are done.
A threshold that is set too high will cause false negatives, when a
signal that is present is note strong enough to pass the threshold.
Similarly, if the threshold value is too low, false positives may be
triggered by noise, whether man-made or otherwise, that exceeds the
threshold. \cite{subramaniam15}

<!--  see subramaniam15 reference [12] for more -->

### Autocorrelation

Autocorrelation function (ACF)


<!--  see subramaniam15 reference [13] for more -->

### Correlation Distance

## Software Defined Radio


A software defined radio peripheral is in simple terms a fast ADC that's
attach to an antenna. SDR platforms are used to digitize a sections
of spectrum which is then either processed in real-time, or it can be
written to non-volatile storage and processing of data can happen at a
later stage.

In an optimal SDR solution the antenna would be essentially connected
directly to the ADC. However, in actual applications it is usually
necessary to implement a radio front end. Typical parts of such a
front end include a bandpass filter (BPF), a low-noise amplifier (LNA)
\cite{needed}



# Materials and Methods

## The Universal Software Defined Radio Peripheral

The USRP is a platform that is designed for research applications
\cite{needed}, and it is evident based on earlier research publications
that is suitable for spectrum sensing applications \cite{angrisani16}.

The USRP has an FPGA that can be used for simple signal processing,
however due to the relatively small size of the FPGA, it is limited in
it's capability, and cannot be used to implement complex PHY layer DPS
blocks. \cite{ni-forum-question}

# Results

# Discussion

# Conclusion
