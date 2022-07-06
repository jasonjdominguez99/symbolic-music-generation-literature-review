# Learning Style-Aware Symbolic Music Representations by Adversarial Autoencoders

## Brief overall summary
### Aim
The aim of the research in this paper was to develop a model which can learn an effective latent space for symbolic music representation. The researcher's definition of effective latent space appears to be that this latent space should encode meaningful music features of a piece, such that a composer could then individually edit these features of the piece with the model. It seems like an attempt at understandable and disentangled latent spaces for music generation.

### Implementation/Method used
The researchers in this paper created a model, named MusAE, based upon an adversarial autoencoder (AAE).

### Achievements
- Reconstruction accuracies better then 'competitor' models.
- First use of AAEs in music generation, which supposedly is useful for more flexibility when choosing the prior distribution of latent vectors (useful for the genre metadata provided for each piece).
- Smooth interpolations between pieces, changing the genre (I believe), between two genres with which the model was trained. "No "holes"" in the latent space which map to unrecognizable examples.
- Latent space organized into low-level characterists of the pianorolls and high-level infor about the music genres.

### Limitations
- Only interpolations are shown to be possible/useable with this model.
- No mention of whether users can generate new music, which pre-selected genre, or complete a piece in a given genre etc., which is more useful a task for composers than interpolations.