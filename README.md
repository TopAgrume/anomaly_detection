The Secure Water Treatment (SWaT) dataset is a critical resource for advancing research in the cybersecurity of Cyber-Physical Systems (CPS). SWaT replicates a scaled-down industrial water treatment facility, providing a realistic platform for exploring both normal operational behaviors and various attack scenarios.
This testbed, capable of producing five gallons of filtered water per minute through ultrafiltration and reverse osmosis, allows researchers to simulate and study complex cybersecurity events.

This project leverages the SWaT dataset to develop a comprehensive data analysis pipeline aimed at anomaly detection and cybersecurity event classification. By addressing the challenges inherent in detecting anomalies and responding to adversarial attacks, this work contributes meaningful insights to the domain of CPS security. The SWaT dataset offers an extensive collection of labeled data encompassing both physical properties and network traffic under normal and compromised conditions, making it an ideal candidate for this study.

## Project objectives
The primary objectives of this project include:
- Detecting anomalies indicative of cyber or physical attacks.
- Benchmarking multiple machine learning algorithms to determine their effectiveness in anomaly detection and classification.
- Exploration on the resilience evaluation of machine learning models against adversarial manipulations.

The insights gained from this analysis will not only enhance the security of CPS like SWaT but also pave the way for designing robust defense mechanisms applicable to other critical infrastructures.
Some papers that were read and studied to gain better insights on the dataset and associated methods can be found in the following list:
- *Jonathan Goh, Sridhar Adepu, Khurum Nazir Junejo and Aditya Mathur*.
  A Dataset to Support Research in the Design of Secure Water Treatment Systems. 11th ICCII, October 2016.
- *Maged Abdelaty, Dr. Domenico Siracusa, Fondazione Bruno Kessler, and Dr. Roberto Doriguzzi-Corin*.
  Robust Anomaly Detection in Critical Infrastructure. ICT, September 2022.
- Mohammed Al-Dhaheri, Ping Zhang, Dina Mikhaylenko
  Detection of Cyber Attacks on a ater Treatment Process. TUK, 2022.

## Dataset: Secure Water Treatment
The Secure Water Treatment (SWaT) dataset is a comprehensive and widely studied dataset in the domain of industrial control systems (ICS) security. It was generated from the Secure Water Treatment testbed, a fully operational scaled-down version of a real-world water treatment plant. The testbed simulates all the essential processes involved in the treatment of water, making it an ideal platform for studying cyber-physical system security.

<img width="1328" height="732" alt="image" src="https://github.com/user-attachments/assets/e0f263c0-9c3f-4415-a72c-7027d3461979" />

The SWaT testbed consists of six distinct stages, each representing critical components of the water treatment process:

- **Raw water storage and transfer (P1)**: Raw water is stored and transferred to the next stage via pumps and motorized valves.
- **Chemical dosing (P2)**: Chemicals are dosed into the water to facilitate coagulation and flocculation.
- **Ultra-filtration (UF) (P3)**: Particulate matter and suspended solids are removed from the water through membranes.
- **Dechlorination (P4)**: Chlorine is removed to make the water safe for consumption.
- **Reverse osmosis (RO) (P5)**: Dissolved salts and impurities are filtered out to produce high-quality permeate water.
- **RO Permeate transfer and UF backwash (P6)**: Treated water is stored and transferred, while periodic backwashing ensures the efficiency of UF membranes.

The dataset provides time-series data from an array of sensors and actuators deployed across these stages, such as flow meters, pressure sensors, water level indicators, and valve statuses. These variables allow researchers to monitor the operational state of the plant in real time. 

## Differents types of anomalies
The SWaT dataset captures various types of anomalies introduced into the system, which can be categorized as follows:

- **Benign:** Normal operational states of the system where all components function within their expected parameters. 
- **Spoofing**: Scenarios where false data is injected into the system, typically to mislead controllers or decision-making algorithms. 
- **Switch\_ON**: Instances where a switch or component is unexpectedly turned on, potentially disrupting the normal sequence of operations. 
- **Switch\_Close**: Situations where a switch is forcefully or incorrectly closed, impacting the flow of processes in the system. 
- **Switch\_Off**: Cases where a switch is turned off inappropriately, halting or interfering with normal operations.

These categories provide a detailed view of the operational and anomalous states captured in the SWaT dataset, making it an essential resource for studying and developing anomaly detection models in industrial systems.

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/eb21c0a5-8756-4ff4-b868-b8eea8178a89" />

### Dataframe breakdown
The dataset used for this project is a subset of the SWaT dataset, containing 14,996 rows and 80 columns. Each row corresponds to a recording of every sensor and actuator in the water treatment plant, spanning from 4:30 AM to 8:40 AM, therefore each entry is sampled at a rate of 1Hz (14996 seconds in total).

These columns provide additionnal context apart from the sensors.
  - **"GMT +0"**: Serves as the index of the DataFrame, each row is a different timestamp.
  - **"Attack"**: Gives context on the type of attack detected for the current row.
  - **"Label"**: Gives a broader information about the security state of the current row.
Finally, **77 columns**: Corresponding to sensors and actuators in the plant. 30 of these 77 columns are irrelevant as they each have a unique value and do not provide useful information.

### Results

<img width="658" height="547" alt="image" src="https://github.com/user-attachments/assets/ebb5f8e9-c4ea-4ae9-b082-b979f92fa197" />
<img width="578" height="453" alt="image" src="https://github.com/user-attachments/assets/1595744b-0a34-40cd-8f43-3d77be2a1907" />
<img width="1525" height="877" alt="image" src="https://github.com/user-attachments/assets/4afac8d2-6f32-4991-af5d-d06c84f26146" />



