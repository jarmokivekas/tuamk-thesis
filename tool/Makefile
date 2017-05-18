


record_test:
	# fft_size is calculated based on sample rate and channel bandwidth
	./usrp_spectrum_sense.py --fft-size 65536 --samp-rate 25000000 629000000 639000000
record_large_test:
	# fft_size is calculated based on sample rate and channel bandwidth
	# each fft takes a lot of time (on order of multiple tens of seconds)
	./usrp_spectrum_sense.py --fft-size 65536 --samp-rate 25000000 529000000 739000000

record_small_fft:
	./usrp_spectrum_sense.py --fft-size 4096 529000000 739000000

overview_test:
	# view the entire DVB-T signal
	./uhd_fft.py --freq  634000000 -s 10000000 --fft-size 4096

detail_test:
	# narrowers possible fft bins available in uhd_fft
	./uhd_fft.py --freq  634000000 -s 200000 --fft-size 4096

detail_8bit_test:
	# narrowers possible fft bins available in uhd_fft
	./uhd_fft.py --freq  634000000 -s 200000 --fft-size 4096 --wire-format sc8

sense:
	./uhd_spectrum_sense -s 10000000 790000000 822000000

show:
	./uhd_fft.py -f 806000000

cfile-high-accuracy:
	uhd_rx_cfile -f 815001000 --samp-rate=195312 --nsamples 100000 "../data/complex-16IQ-195412-$(date --iso-8601=s)"
