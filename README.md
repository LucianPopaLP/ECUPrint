# ECUPrint Dataset

The ECUPrint dataset is a collection of raw CAN voltage samples and CAN logs. Skew and voltage data is collected from 10 vehicles, ranging from small cars to SUVs and a heavy-duty vehicle, totaling 54 ECUs. In order to enable the CAN data collection we employed two devices: a CANcaseXL and a Pico Scope 5000 Series. The voltage collection setup is shown below: the CAN bus is accessed via the OBD-II pins with the previously mentioned tools.

![Data collection setup](https://github.com/LucianPopaLP/ECUPrint/blob/main/images/voltage_setup.png?raw=true)

If you use or discuss our dataset in your work, please cite our paper (bibtex citation below).  A PDF link for our paper can be found at [TBD].

## Voltage data ##

For each frame carrying a specific ID we have collected samples for an isolated dominant bit which is a transition from recessive to dominant and back (the shape of an isolated bit, along with the features we extract is shown below). We use the following voltage features: i) the mean voltage level, ii) max voltage level and iii) bit time. In addition to these, which are commonly used in other works, we also note that the iv) plateau time of the bit also provides good indications on the sender ECU, so we introduce this as an additional metric.

![Raw voltage sample and voltage features](https://github.com/LucianPopaLP/ECUPrint/blob/main/images/voltage_369_bis.png?raw=true)

## Skew data ##

To extract the clock skews, we use the CAN logs which contain the frame identifiers and associated timestamps. In order to perform data collection for skews we used the XL Driver Library and recorded the available CAN frames through the diagnostics port. We logged CAN traffic over periods of 5 to 10 minutes for each vehicle while it was operational.

Skews provide a good separation for ECUs in the same vehicle as shown in the image below.

![Skew based inter-distances and intra-distances](https://github.com/LucianPopaLP/ECUPrint/blob/main/images/skews_all_distances.png?raw=true)

When merging multiple features, i.e., the mean, max, bit and plateau time, the overlaps almost fully disappear as the image below shows.

![Voltage based inter-distances and intra-distances](https://github.com/LucianPopaLP/ECUPrint/blob/main/images/voltage_all_distances.png?raw=true)

## Dataset content ##

The dataset is structured as described below. We provide the raw CAN voltage samples measured with the PicoScope with a sample interval of 2 nanoseconds (sample rate was set to 500 MS/s) and separate CAN logs with frames collected with a Vector CANCaseXL device. For Honda Civic and Ford Fiesta there are two sets of raw CAN voltage samples and two CAN logs. The first set was collected after vehicle startup (cold engine) and the second after 1 hour drive (warm engine).

<ol type="a">
  <li>CAN logs (note that the log file contains several additional IDs for John Deere, Ford Ecosport and Fiesta which were on-event and voltage data cannot be retrieved for all of them or they could not associated to a specific ECU)</li>
  <li>CAN voltage samples for 10 cars (data is also allocated to specific ECUs based on the analysis in our work, note that this distribution is to the best we could ascertain. Note that there are several bits in a folder named Unclassified since these are on-event and skews could not be computed them) (181,874 sampled bits)</li>
  <li>CAN voltage samples under environmental variations for 2 cars (Ford Fiesta and Honda Civic) (47,636 sampled bits)</li>
  <li>all voltage as a single archive (229,510 sampled bits)</li>
</ol>

## Data links ##

File | Download | Version | Date | Notes
---- | :------: | :-------: | :--------: | :------
**[ECUPrint] CAN logs.zip** | [link]() | 1.0 | 02/26/2022 | ECUPrint complete dataset
**[ECUPrint] CAN voltage samples with ECU allocation** | [link]() | 1.0 | 02/26/2022 | ECUPrint Dacia Duster dataset
**[ECUPrint] CAN voltage samples under environmental variations.zip** | [link]() | 1.0 | 02/26/2022 | ECUPrint Dacia Logan dataset
**[ECUPrint] CAN voltage samples (full).zip** | [link]() | 1.0 | 02/26/2022 | ECUPrint Ford Ecosport dataset

## Data Organization

There are raw voltage data files for 54 ECUs and 433 IDs from 10 different vehicles, one of them being a heavy-duty vehicle that is compliant to the SAE J1939 standard. They are structured per-vehicle and per-ECU as they were identified in our work.

## Contacts
* lucian.popa [at] aut.upt.ro
* bogdan.groza [at] aut.upt.ro
