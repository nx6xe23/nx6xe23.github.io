---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

---

<details>
<summary> <p style="font-size:24px; display:inline">RTLGenBench</p>
<br>
A Framework to systematically benchmark LLM-based RTL generation
</summary>
<br>
<img src="/images/rtlgenbench.png" style="float:right;" height=400 width=400>

This work is done under the guidance of Prof. Vijay Janapa Reddi. The goal of this project is to develop a framework for benchmarking LLMs in their ability to generate RTL design. This tool is a part of the larger project of developing foundational models for hardware design. Since there is less work done in the field of benchmarking LLMs for RTL generation, this project aims to fill that gap. The tool is designed to test the LLMs on their ability to generate RTL code for a given design. The tool is modular in design, with the ability to test different LLMs on different designs. The tool is designed to be user-friendly, with the user only needing to provide the design specification and the LLM to be tested.
<br><br>
The tool systematically prompts the LLM using five different prompt techniques, namely, zero shot, few shot, chain of thought, raw context, and summarized context mode. The tool then handles the generated RTL and checks syntax, and correctness through simulation tests at module as well as complete design level. There are 3 different difficulty levels the LLM can be tested on, namely, easy (1 code line insertion), medium (4-6 code line insertion), and hard (full module generation). Furthermore, we are planning on integrating it with SiliconCompiler, to test if the design is synthesizable.
</details>
---
<details>
<summary> <p style="font-size:24px; display:inline">
Smart Connected Buildings</p><br>
Using machine learning to build solutions for data loss and privacy in smart meters.
</summary><br>
<img src="/images/smdata.png" style="float:left;" height=400 width=400>

This project was conducted under the guidance of Prof. Anupama Kowli and aimed to investigate and develop solutions for challenges related to smart meters in connected buildings. The primary issues addressed were data loss due to network instability and security concerns arising from the high volume of data generated by smart meters, which ranges in granularity from seconds to minutes.
<br><br>
To address security concerns, we trained machine learning models to predict household appliances based on electricity consumption patterns. Using 15-minute, daily, and monthly consumption data from 116 households across India, we applied random forest, XGBoost, and multi-layer perceptron models. Results indicated a strong correlation between consumption patterns and household appliances, achieving prediction accuracy between 70% and 80%. While higher data granularity did not significantly boost accuracy, incorporating daily temperature data did lead to improvements.
<br><br>
To address data loss, we experimented with various statistical and machine learning-based imputation techniques, achieving a best model performance of 6% MAPE. The most effective approach combined statistical and machine learning methods, outperforming alternatives such as GANs, autoencoders, and random forest. Our imputation strategy used standard interpolation for single missing data points, while a combination of historical averaging and linear interpolation was applied for gaps under a day. For missing data spanning more than a day, KNN emerged as the most effective technique.
<br><br>
To further address privacy concerns, we developed models to predict half-hourly load profiles for both individual and clustered households using only monthly consumption and time-of-use tariff data. For clustered households, the model achieved a 7% NMAE using monthly consumption data. This approach allows us to substitute individual half-hourly data with aggregated monthly data for clusters of households, with minimal loss in accuracy. By using less granular, aggregated data, we effectively reduce privacy risks associated with fine-grained household consumption records.
</details>
---
<details>
<summary> <p style="font-size:24px; display:inline">
ArchGym</p><br>
An OpenAI Gymnasium for Machine Learning Assisted Architecture Design
</summary><br>
<img src="/images/archgym.png" style="float:right;" height=400 width=400>

This project was conducted under the guidance of Prof. Vijay Janapa Reddi, aiming to extend the ArchGym framework to support a range of hardware accelerators. My work centered on integrating the AstraSim simulator into ArchGym. As a cycle-accurate simulator for neural network accelerators, AstraSim enhances ArchGym’s capabilities, enabling users to apply multiple machine learning algorithms to fine-tune accelerator designs and significantly optimize results.
<br><br>
Additionally, I developed a machine learning proxy pipeline to predict accelerator performance based on input parameters. This pipeline is trained on datasets generated from running accelerator designs on AstraSim via ArchGym. It provides a range of models, including all Scikit-Learn models, XGBoost, and NODE, and is designed with a modular structure, allowing users to seamlessly switch between different models and hyperparameters to optimize predictions.
</details>
---
<details>
<summary> <p style="font-size:24px; display:inline">
Transforming Breast Cancer Diagnosis</p><br>
Towards Real-Time Ultrasound to Mammogram Conversion for Cost-Effective Diagnosis
</summary><br>
<img src="/images/medal.png" style="float:left;" height=400 width=400>

This project, conducted under the guidance of Prof. Amit Sethi, focused on designing a system to transform ultrasound images into mammogram-like images, a development aimed at advancing real-time breast cancer diagnosis. Ultrasound imaging is commonly used for breast screenings due to its non-invasive nature and accessibility, but it lacks the detailed tissue contrasts seen in mammograms, which are highly valuable for detecting abnormalities. By converting ultrasound images to a mammogram-like format, this system seeks to combine the benefits of ultrasound imaging with the diagnostic accuracy of mammograms, providing clinicians with a potentially more informative tool for breast cancer detection.
<br><br>
To accomplish this, we utilized CycleGAN and pix2pix deep learning models, both well-suited for image-to-image translation tasks. These models were trained to convert ultrasound images into mammogram-like images by learning from paired image datasets, achieving a mean squared error (MSE) of 0.008, indicating high-quality synthetic outputs. Preprocessing involved transforming computed tomography (CT) scans into speed-of-sound (SoS) images, which simulated ultrasound images through wave interference equations. This simulation, conducted using the Stride module, provided a more realistic dataset for model training, helping bridge the gap between ultrasound and mammogram image characteristics.
<br><br>
To further improve image quality, we applied Fourier Domain Adaptation, a technique designed to enhance the fidelity of simulated ultrasound images when compared with authentic ultrasound scans. This adaptation aligns the spectral properties of simulated images with those of real ultrasound images, reducing artifacts and improving realism. By integrating these methods, the project produced a robust system for generating mammogram-like images from ultrasound data, paving the way for enhanced diagnostic capabilities in breast cancer screening.

</details>
---
<details>
<summary> <p style="font-size:24px; display:inline">
Exploring In-Memory Object Stores and ANN Indexing</p>
</summary><br>
This project was conducted under the guidance of Prof. Dixin Tang. I
extensively researched in-memory object stores within Ray, an open-source framework for scaling machine learning workloads, building distributed systems, and deploying large-scale applications. This project focused on optimizing Ray's object store to enhance performance, with particular emphasis on its data management strategies. Additionally, I studied Ray's Distributed Data Parallel module and its role in training deep neural networks, as well as the use of relay buffer memories and object stores in reinforcement learning algorithms, such as DQN.
<br><br>
The research included an in-depth exploration of data communication mechanisms between processes in distributed systems, particularly the data transfer methods within Ray’s object store. I also investigated the potential applications of Compute Express Link (CXL) to enable high-level data sharing, providing insights into advanced data handling strategies in distributed machine learning environments.
<br><br>
Additionally, I investigated the use of approximate nearest neighbor (ANN) indexing in machine learning applications, particularly focusing on the FAISS library. This research aimed to understand the core principles of ANN indexing and explore optimization strategies for improved performance. I also studied Starling, a system that leverages disk storage for ANN indexes, and examined the potential of using Parquet files to store these indexes in a distributed format, enabling more efficient data access and scalability in large-scale applications.
</details>
---