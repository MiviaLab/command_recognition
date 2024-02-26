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

## Instructions
1. Clone the repository.
2. Follow the provided instructions to set up the environment.
3. Use the training code to reproduce the Speech-Command Recognition system.
4. Access the dataset for experimentation.
5. Evaluate system performance with the provided test code.

Feel free to explore, replicate experiments, and contribute to the development of this efficient embedded Speech-Command Recognition system.

## Reference
'''bibtext
'''
