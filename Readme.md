The project is about a classification task of Radar signals. 

### Context

You command a reconnaissance aircraft on a top secret mission. Despite your discretion and all the precautions taken, you are disturbing and may be the subject of threats that you must detect to guarantee the safety of your crew and the success of your mission (as it is top secret, you cannot find out more).

At your disposal a network of antennas and an advanced spectral analysis system allow you to extract and characterize signals from the radars at altitude 0 which dot your route.

A radar signal is made up of pulses. The analysis system allows you to characterize each pulse received by a PDW (Pulse Description Word) which contains:

- the pulse detection start date (in ms)
- the width or duration of the pulse (in ms)
- the power of the pulse (in dB / reference)
- the theta angle and the phi angle describing the direction in which the pulse is detected (in radians)
- the pulse frequency (in Ghz)

Your sensor is not perfect and you are notably experiencing a scattering phenomenon: a certain proportion of the pulses emitted are not detected. This proportion is all the greater as the power of the pulses is small.

Your ship is sailing at an altitude of 10 km, with a constant speed of 1000 km/h towards the north.

Previous missions have produced a 10-second signal database.
Each signal comes in the form of an .npz file which contains all the PDWs received.

A signal is therefore a file whose name is of the form 'pdw_<signal number>.npz'.

This database is annotated: the fate of each mission allowed to declare each signal as a 'threat' or a 'non-threat'.

The signals were split into two independent sets:
- train
- test
 
The annotations for each set are available in the labels_<train or test>.json file which gives the filename -> threat or non-threat label.