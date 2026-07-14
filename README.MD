# Variational Autoencoder for Respiratory Sound Analysis

An unsupervised deep-learning project for learning compressed representations of respiratory sound recordings using a Variational Autoencoder (VAE).

## Project Overview

Respiratory recordings contain complex acoustic patterns associated with normal breathing, wheezes, crackles and other respiratory conditions. This project explores how a Variational Autoencoder can learn meaningful latent representations from respiratory audio without relying entirely on labelled data.

The project uses respiratory recordings from the ICBHI respiratory sound database. Audio recordings are prepared as machine-learning-ready representations, passed through a VAE and reconstructed by the decoder. The learned latent space and reconstruction behaviour are then analysed.

This project was completed as part of the CSE427 Neural Networks course at BRAC University.

## Objectives

- Prepare respiratory audio recordings for deep-learning analysis.
- Train a Variational Autoencoder on respiratory sound representations.
- Learn compact latent features from high-dimensional audio data.
- Analyse reconstruction quality and training behaviour.
- Explore patterns within the learned latent space.
- Investigate the suitability of VAEs for respiratory-sound representation learning.

## Methodology

The project follows the following workflow:

1. Load respiratory recordings from the ICBHI dataset.
2. Inspect and preprocess the audio data.
3. Convert recordings into consistent numerical representations.
4. Normalise and prepare the data for model training.
5. Divide the prepared data into training and evaluation sets.
6. Construct the VAE encoder, latent space and decoder.
7. Train the model using reconstruction loss and KL-divergence loss.
8. Reconstruct respiratory-sound representations.
9. Analyse the model’s training history, reconstructions and latent patterns.

## Variational Autoencoder

The VAE contains three main components:

### Encoder

The encoder transforms the respiratory-sound input into two vectors:

- Latent mean
- Latent log variance

These vectors define a probability distribution in the latent space.

### Sampling Layer

The reparameterisation trick is used to sample latent vectors while allowing the model to be trained through backpropagation.

### Decoder

The decoder reconstructs the respiratory-sound representation from the sampled latent vector.

The training objective combines:

- Reconstruction loss
- Kullback-Leibler divergence loss

## Dataset

The project uses respiratory recordings from the **ICBHI Respiratory Sound Database**.

The dataset contains recordings collected from different participants and includes normal and abnormal respiratory sounds recorded using different respiratory-auscultation devices.

Dataset usage remains subject to the original dataset licence and conditions.

## Repository Structure

```text
Variational-Autoencoder-for-Respiratory-Sound-Analysis/
│
├── ICBHI_final_database/
│   └── Respiratory audio recordings and annotation files
│
├── Section_01_Group_03_ID_22241108_22201441_.ipynb
│   └── Complete preprocessing, VAE training and analysis notebook
│
├── Section_01_Group_03_ID_22241108_22201441.pdf
│   └── Project report
│
├── requirements.txt
│   └── Required Python libraries
│
└── README.md

Technologies Used :
Python
Jupyter Notebook
TensorFlow / Keras
NumPy
Pandas
Matplotlib
Librosa
Scikit-learn
Variational Autoencoders
Audio signal processing
Installation

Clone the repository:
git clone https://github.com/prithu011/Variational-Autoencoder-for-Respiratory-Sound-Analysis.git
cd Variational-Autoencoder-for-Respiratory-Sound-Analysis

Project Outputs :

The notebook produces outputs such as:
Respiratory-audio preprocessing summaries
Model architecture information
VAE training and validation losses
Reconstruction-loss analysis
Original and reconstructed representations
Latent-space visualisations
Analysis of learned respiratory-sound patterns

Limitations:
The project is intended for academic and research purposes.
Results depend on preprocessing choices, model configuration and dataset quality.
The dataset contains class and recording-condition variations.
The model is not intended to provide clinical diagnoses.
Medical interpretation would require validation by qualified healthcare professionals.

Future Improvements:
Experiment with convolutional VAE architectures.
Compare VAEs with standard autoencoders.
Use Mel-spectrograms as model inputs.
Evaluate Beta-VAE and conditional VAE architectures.
Apply clustering to the learned latent representations.
Investigate anomaly detection for abnormal respiratory sounds.
Compare latent features with supervised classification models.
Use patient-independent train and test splits.

Authors
Tanjum Ibnul Mahmud


