
# Installation and configuration



Notes in this section are largely based on the Ettus wiki article [on how to verify operation of the USRP](https://kb.ettus.com/Verifying_the_Operation_of_the_USRP_Using_UHD_and_GNU_Radio)



Initially set the Ethernet interface address manually to 192.168.10.1/24.


```
> uhd_find_devices
linux; GNU C++ version 5.3.1 20151219; Boost_105800; UHD_003.009.002-0-unknown

--------------------------------------------------
-- UHD Device 0
--------------------------------------------------
Device Address:
    type: usrp2
    addr: 192.168.10.2
    name:
    serial: F40FE6
```


on Ubuntu examples can be located at `/usr/lib/uhd/examples` as well as `/usr/share/gnuradio/examples/uhd`.

To test your installation, move to the `/usr/lib/uhd/examples` directory
and execute the benchmark_rate program

    ./benchmark_rate --rx_rate 10e6 --tx_rate 10e6


# Calibrating IQ sample balance


# Spectrum Sensing

The gnu radio examples have python script that can be used for simple monitoring:

    ./usrp_spectrum_sense.py  791000000 821000000
