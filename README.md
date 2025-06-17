# Nuclear Event Detector - bhangmeterv2

![Untitled-1](https://github.com/user-attachments/assets/c01477d0-82af-4875-ba32-bf114a4e8395)

The BhangmeterV2 is a RaspberryPiPico2W powered device which detect the gamma ray burst from a nuclear explosion and uploads the details into a JSON

# How does it work?

The Bhangmeter V2 employs an HSN-1000L Nuclear Event Detector to register the initial gamma ray burst from a nuclear explosion. This burst travels at the speed of light and reaches the detector almost instantly. It is followed shortly by the neutron flux—traveling at roughly 10% the speed of light—and then the blast wave, which moves much slower at Mach 1.5 to 3, arriving several milliseconds to seconds later depending on the distance.

![blast_to_diode](https://github.com/user-attachments/assets/2bece322-5ea8-42a5-8049-cbf15bcab559)

The HSN-1000L detects the gamma burst and outputs an active-low pulse, which the microcontroller interprets as a "Nuclear Event Detection" (NED). This triggers a routine that logs the exact time of the event.

![computer](https://github.com/user-attachments/assets/aab75a1a-f552-4dfd-8801-7d6a44f75b4a)

Once detected by the onboard computer, the NED timestamp is uploaded to the cloud for permanent storage.

![cloud](https://github.com/user-attachments/assets/db108309-35af-473e-91ee-56fc62db3a8e)

A short time later—depending on the distance from the detonation site—the blast wave reaches the Bhangmeter V2, marking the completion of its mission. Its specialized polymer casing provides brief ablative cooling upon impact.

![destruct](https://github.com/user-attachments/assets/f742e814-d996-41aa-b983-b5ae7cac90e1)

# Software Setup

To setup the raspberry pi load micropython from https://micropython.org/download/

Once loaded put the main.py and secrets.py into the micropython environment.

You will need to update the secrets file with your wifi details, your github token and the path to the repo where the .json is stored

# Mechanical Build

![Build_Instructions_bh](https://github.com/user-attachments/assets/79fe3f5b-c295-4410-a7aa-454044795b2e)

