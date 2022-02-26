# ECUPrint Dataset

The ECUPrint dataset is a collection of raw CAN voltage samples measured with the PicoScope with a sample interval of 2 nanoseconds (sample rate was set to 500 MS/s) and CAN logs with frames collected with a Vector CANCaseXL device.

If you use or discuss our dataset in your work, please cite our paper (bibtex citation below).  A PDF link for our paper can be found at [http://www.aut.upt.ro/~bgroza/Papers/j1939_fprint.pdf](http://www.aut.upt.ro/~bgroza/Papers/j1939_fprint.pdf).

```
@article{Popa21ECUPrint,
title={ECUPrint - Physical Fingerprinting Electronic Control Units on CAN Buses inside Cars and SAE J1939 Compliant Vehicles},
author={Popa, Lucian and Groza, Bogdan and Jichici, Camil and Murvay, Pal-Stefan},
journal={IEEE Transactions on Information Forensics & Security},
year={2021},
publisher={IEEE}
}
```

## Data links ##

File | Download | Version | Date | Notes
---- | :------: | :-------: | :--------: | :------
**ecuprint_dataset_v1.0.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint dataset


## Data Organization

There are raw voltage data files for 54 ECUs and 433 IDs from 10 different vehicles, one of them being a heavy-duty vehicle that is compliant to the SAE J1939 standard. They are structured per-vehicle and per-ECU as they were identified in our work.

## Contacts
* lucian.popa [at] aut.upt.ro
* bogdan.groza [at] aut.upt.ro
* camil.jichici [at] aut.upt.ro
* pal-stefan.murvay [at] aut.upt.ro
