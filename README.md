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
**ecuprint_complete_dataset.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint complete dataset
**ecuprint_dacia_duster_dataset.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Dacia Duster dataset
**ecuprint_dacia_logan_dataset.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Dacia Logan dataset
**ecuprint_ford_ecosport.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Ford Ecosport dataset
**ecuprint_ford_fiesta.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Ford Fiesta dataset
**ecuprint_ford_kuga.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Ford Kuga dataset
**ecuprint_honda_civic.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Honda Civic dataset
**ecuprint_hyundai_i20.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Hyundai i20 dataset
**ecuprint_hyundai_ix35.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Hyundai ix35 dataset
**ecuprint_john_deere_tractor.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint John Deere tractor dataset
**ecuprint_opel_corsa.tar** | [link]() | 1.0 | 02/26/2022 | ECUPrint Opel Corsa dataset


## Data Organization

There are raw voltage data files for 54 ECUs and 433 IDs from 10 different vehicles, one of them being a heavy-duty vehicle that is compliant to the SAE J1939 standard. They are structured per-vehicle and per-ECU as they were identified in our work.

## Contacts
* lucian.popa [at] aut.upt.ro
* bogdan.groza [at] aut.upt.ro
