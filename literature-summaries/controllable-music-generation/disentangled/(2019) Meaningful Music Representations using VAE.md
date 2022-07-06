# Inspecting and Interacting with Meaningful Music Representations using VAE

## Brief overall summary
### Aim
The aim of the research done in this paper was to create a music generation model, specifically a VAE like MusicVAE, with disentangled rhythm and pitch in the latent space, to allow for the control of these features. The method created to perform this disentanglement is refered to as 'disentanglement by augmentation'.

### Implementation/Method used
The model is based upon MusicVAE. This is a VAE which utilizes LSTMs and is designed for 2-bar sequences of 4/4 MIDI data. In order to have an interpretable latent space, the latent space dimensions were reduced compared to the original MusicVAE model. PCA was performed on the data, to decide that reducing the dimensions from 512 to 128 would work.
Disentanglement by augmentation starts from a well-trained MusicVAE model. The idea is that a function which augments an input music clip has a corresponding function which alters the latent space representation. They assume that only a few latent space dimensions are significantly changed in an operation and find these by varying pitch and seeing which axes repsond most and similarly for rhythm.

### Achievements
- Successful disentanglement of pitch and rhythm, but this has since been improved upon.

### Limitations
- More complex latent space manipulations are not interpretable
- Disentanglement comes after training, this is improved upon with [[(2019) DEEP MUSIC ANALOGY]], in which the model is trained to have a disentangled latent space.