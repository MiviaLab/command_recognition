# Embedded Speech-Command Recognition for Noisy Industrial Environments

Welcome to the GitHub repository for the code supporting our publication in [Journal Name]. This repository contains the implementation of a Speech-Command Recognition system tailored for embedded devices in noisy industrial settings.

**Abstract:**
Communication between robots and humans in industrial environments heavily relies on speech, presenting challenges in high-noise scenarios. Our work addresses this by introducing a Speech-Command Recognition system optimized for embedded devices with limited computational resources. Using an innovative End-to-End architecture based on the ResNet backbone, our solution achieves high accuracy while minimizing computational burden. We implement Curriculum Learning and dynamic data augmentation to enhance robustness against noise during training.

**Key Features:**
- **Embedded Device Optimization:** Tailored for devices with limited computational capabilities, ensuring real-time performance in industrial environments.
- **End-to-End Architecture:** Innovative ResNet-based architecture for optimal accuracy with minimal computational load.
- **Curriculum Learning:** Progressive learning strategy to handle increasing sample complexities.
- **Dynamic Data Augmentation:** Techniques to introduce noise during training, improving system robustness.

**Dataset:**
- A comprehensive dataset of over 50,000 samples, including real-world data from daily operations at a Stellantis Italian factory.

**Model Size and Inference Speed:**
- Achieves impressive accuracy rates exceeding 90% for both English and Italian commands.
- Compact model size: 1.81 MB.
- Real-time inference on embedded devices: 41 ms on an NVIDIA Xavier NX.

**Repository Contents:**
1. **Training Code:** Implementation of the Speech-Command Recognition system, including Curriculum Learning and dynamic data augmentation.
2. **Dataset:** Access to the dataset used for training and testing.
3. **Test Code:** Code for evaluating the system's performance and conducting inference.

## Dataset
The Mivia Industrial Speech-Commands (MISC) dataset, developed at the MIVIA laboratory of the University of Salerno in collaboration with the CRF of the Stellantis automotive group, is a comprehensive dataset specifically designed for training Speaker Command Recognition (SCR) systems in industrial environments. This dataset encompasses 31 commands recorded in both English and Italian languages, intended for controlling various aspects of a robot or workstation on a production line. Examples of commands include "move forward", "take me the screwdriver", "increase the illumination", and more.
The dataset comprises various types of samples, including:
- **9,342 "real" samples pronounced by authentic speakers** (218 English and 222 Italian). These samples were recorded through a Telegram bot under noiseless conditions, enabling data collection from diverse acquisition devices and increasing data variability.
- **1,984 "industrial real" samples pronounced by authentic speakers** (16 English and 16 Italian) on the production line of Stellantis plants. Unlike the samples captured using the Telegram bot, which are clean samples with artificially added noise, those in this dataset are real and noisy samples collected directly from the industrial production line. These additional samples serve as valuable resources for testing the system in a real-world scenario. The testing dataset was collected during the daily operations of the industry, utilizing two different microphones placed at varying distances. The first microphone used is a ReSpeaker micArray v1, positioned near the worker at a distance of 1-2 meters. The second microphone is the embedded microphone of a laptop, positioned further away from the worker at a distance of 3-4 meters.
- **5,084 "synthetic" samples generated using Text-to-Speech systems** such as Amazon Polly, Google Cloud, Azure, Nvidia Nemo, Vocalware, and Naturalreaders. This includes 144 English and 20 Italian synthetic speakers.
- **32,265 "reject" samples**, namely chatter that doesn't include the defined commands and background noises. This part consists of 20,083 samples from the Google Speech-Commands dataset, 9,551 from Mozilla Common Voices, and 2,635 noisy samples (further described in the next point). 
- **2,635 "noisy" samples**, further categorized into two groups. The first group comprises 1,604 samples acquired in the Stellantis plant during a typical working day, representing real-world industrial noise. The second group includes 1,031 samples sourced from the FreeSound dataset.
Specifically, the subset derived from in-plant acquisitions is labeled the Mivia In-Plant Industrial Speech Commands dataset, abbreviated as the MiPISC dataset.

## Instructions
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/MiviaLab/command_recognition.git
   ```
2. **Configure Training Settings:**
   Modify the "conf.py" file located at "./training/settings." This file contains all the parameters necessary for the training and testing phases, such as model configuration, curriculum learning strategy, training parameters, etc.
3. **Train the Speech-Command Recognition System:**
   In the "training" folder, execute the "train.py" script by providing the configuration file (e.g., "conf.py") for training.
   ```bash
   python3 train.py --configuration conf
   ```
4. **Evaluate System Performance:**
   Evaluate the system's performance using the provided test code. From the "training" folder, run the "test.py" script by passing the configuration file (e.g., "conf.py") for testing.
   ```bash
   python3 test.py --configuration conf
   ```

## Reference
```bibtext
```
