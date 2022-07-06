# CONLON: A PSEUDO-SONG GENERATOR BASED ON A NEW PIANOROLL, WASSERSTEIN AUTOENCODERS, AND OPTIMAL INTERPOLATIONS

## Brief overall summary
### Aim
The researchers aimed to develop a symbolic music generation method which was more practically useful for musicians than other techniques (This is similar to one of my project aims). Specifically, they focused on 'pseudo-song' generation via interpolation.

### Implementation/Method used
The deep learning architecture used was a Wasserstein Autoencoder (WAE). The generation method involves selecting a start and end 'test pattern' and traversing the latent space of the WAE to interpolate between the patterns. This produces a steadily evolving piece of music, which is refered to as a 'pseudo-song' as it lacks form and is closer to improvisation. Through training on carefully selected datasets containing a few genres, generated interpolations can evolve from one genre to another.

### Achievements
- First application of WAEs to music generation which helps tackle 'blurriness' problem of traversing a latent space. This problem is explained as coming from selecting latent vectors, during intepolation, which are very close in latent space. For music generation this can result in "large clusters of notes being played together".
- Creation of a new lossless pianoroll-like data description. This is capable of storing velocity (volume) and duration information for notes. The researchers say that this can be convert to MIDI making is useful for musicians.
- Subjectively evaluated to be more useful to musicians than another leading model MuseGAN ([[(2017) MuseGAN]]) by 69.
- Compilation of carefully selected datasets of music patterns, being careful too avoid a large range of musical genres, so that generated models are more targeted to their require genre generation.

### Limitations
- A single model is trained on a dataset specific to one, or only a few genres. Genre selection from a single trained model is not possible.
- No form. The interpolation between test patterns does not result in songs with form, hence the use of the term 'pseudo-song' generation.
- Limited control over the music generated. In terms of application, the generation method seems more akin to randomly generating similar music and seeing if something 'good' is generated, rather than composers being involved in the process, requiring specific constraints in the generation.
- Although genre is mentioned, it is not clear whether there is any selection possible (i.e. understandibility of the latent space) with respect to genre, or genre specific characteristics.
- Instrumentation, which is very indicative of genre/style and very useful for a composer, does not seem to be controllable.