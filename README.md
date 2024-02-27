# Embedded Speech-Command Recognition for Noisy Industrial Environments

Welcome to the GitHub repository for the code supporting our publication in [Journal Name]. This repository contains the implementation of a Speech-Command Recognition system tailored for embedded devices in noisy industrial settings.

**Abstract:**
Communication between robots and humans in industrial environments heavily relies on speech, presenting challenges in high-noise scenarios. Our work addresses this by introducing a Speech-Command Recognition system optimized for embedded devices with limited computational resources. Using an innovative End-to-End architecture based on the ResNet backbone, our solution achieves high accuracy while minimizing computational burden. We implement Curriculum Learning and dynamic data augmentation to enhance robustness against noise during training.

**Key Features:**
- **Embedded Device Optimization:** Tailored for devices with limited computational capabilities, ensuring real-time performance in industrial environments.
- **End-to-End Architecture:** Innovative ResNet-based architecture for optimal accuracy with minimal computational load.
- **Curriculum Learning:** Progressive learning strategy to handle increasing sample complexities.
- **Dynamic Data Augmentation:** Techniques to introduce noise during training, improving system robustness.

**Repository Contents:**
1. **Training Code:** Implementation of the Speech-Command Recognition system, including Curriculum Learning and dynamic data augmentation.
2. **Dataset:** Access to the dataset used for training and testing.
3. **Test Code:** Code for evaluating the system's performance and conducting inference.

## Dataset
The Mivia Industrial Speech-Commands (MISC) dataset, created at the MIVIA lab in collaboration with Stellantis, is designed for training Speaker Command Recognition (SCR) systems in industrial settings. It features 31 commands in English and Italian, controlling robots or workstations in production lines. The dataset includes:
- **9,342 "real" samples** recorded via a Telegram bot in noiseless conditions, providing diverse data sources.
- **1,984 "industrial real" samples** captured on Stellantis production lines, offering real and noisy scenarios for system testing.
- **5,084 "synthetic" samples** generated using Text-to-Speech systems from various providers.
- **32,265 "reject" samples** containing background noise and irrelevant chatter from different datasets.
- **2,635 "noisy" samples**, including real-world industrial noise from the Stellantis plant and additional samples from the FreeSound dataset.

The subset from in-plant acquisitions is named the Mivia In-Plant Industrial Speech Commands dataset (MiPISC).

## Instructions
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/MiviaLab/command_recognition.git
   ```
2. **Configure Training Settings:**
   Modify the "conf.py" file located at "./settings." This file contains all the parameters necessary for the training and testing phases, such as model configuration, curriculum learning strategy, training parameters, etc.
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
