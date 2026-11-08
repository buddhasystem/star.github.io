---
title: "Front End Electronics (FEE)"
redirect_from:
  - /public/fee/
  - /public/fee/fee.html
---

*Last updated December 2, 2002.*

This is the home page for the Front End Electronics Subsystem. The Front End Electronics is discussed in a [paper](http://arxiv.org/abs/nucl-ex/0205014){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> that will appear in a volume of Nucl. Instrum. & Meth. devoted to RHIC.

## Topics

[An early Overview](https://www.star.bnl.gov/public/fee/feeover.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> of the FEE system is given in "Front End Electronics for the STAR TPC", S.Klein etal., [STAR Note 0239](https://www.star.bnl.gov/star/starlib/doc/www/sno/ice/sn0239.html){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>, published in IEEE Transactions on Nuclear Science 43, 1768 (1996). Some of the system requirements are given in the [essential model](https://www.star.bnl.gov/public/fee/FEE_Funct_Req.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>.

### [FEE card](https://www.star.bnl.gov/public/fee/feeboard.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> ([photo](https://www.star.bnl.gov/public/fee/feecard.jpg){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>)

The FEE card holds two chips, the SAS preamplifer/shaper, and the SCA switched capacitor array, together with associated components. Each FEE card holds two of each chip, servicing 32 TPC readout channels.

### [SAS chip](https://www.star.bnl.gov/public/fee/sas.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>

The SAS chip contains 16 channels of integrating preamplifer plus shaper. The chip is more fully described in [STAR Note 0230](https://www.star.bnl.gov/star/starlib/doc/www/sno/ice/sn0230.html){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>, "A Low Noise Amplifier-Shaper with Tail Correction for the STAR Detector", E. Beuville etal., published in the IEEE Transactions on Nuclear Science 43, 1619 (1996).

### [SCA chip](https://www.star.bnl.gov/public/fee/sca.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>

The SCA chip holds a 16 channel wide, 512 deep switched capacitor array, together with a 12 bit ADC.

### [Readout Board](https://www.star.bnl.gov/public/fee/readout.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> ([photo](https://www.star.bnl.gov/public/fee/rdo.jpg){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>)

The readout board provides power to the FEE boards, accepts signals from them, buffers the signals, and transmits the signal off of the detector via fiber optic cables.

The readout board includes a 1 Mbit/sec HDLC link, described in [STAR Note 0241](https://www.star.bnl.gov/star/starlib/doc/www/sno/ice/sn0241.html){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>; the link handles readout board control and monitoring, and can serve as an alternate slow data readout path. A [schematic](https://www.star.bnl.gov/public/fee/hdlc.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> of the link is available, along with [a motherboard design](https://www.star.bnl.gov/public/fee/hdlcm.ps){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span> and a [list of signals](https://www.star.bnl.gov/public/fee/HDLC_signals.txt){:target="_blank" rel="noopener"}&nbsp;<span data-feather="external-link"></span>.

For further information contact: Spencer Klein
