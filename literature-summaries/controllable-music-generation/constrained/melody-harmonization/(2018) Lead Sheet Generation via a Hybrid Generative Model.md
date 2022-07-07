# Lead Sheet Generation and Arrangement via a Hybrid Generative Model

## Brief overall summary
### Aim
This research aimed to tackle the task of lead sheet arrangement, a task between that of lead sheet generation (creating a melody with accompanying chords) and accompaniment generation (creating tracks for different instruments, playing different parts).

### Implementation/Method used
Lead sheet generation is performed using a VAE. The arrangement generation part of the model then extracts features from the generated lead sheet and inputs them into a conditional GAN.

### Achievements
- First attempt at combining areas of lead sheet generation and accompaniment generation.

### Limitations
- Only 8 bars generated
- Restricted to 4/4 time signature
- Existing chord recognition model used, which could have its own limitations.
- Not clear if generation can be subject to a prior, user given, chords, or melody and have the missing one generated. Seems like from scratch.
- Unclear whether extended chords are used for harmonization/accompaniment.