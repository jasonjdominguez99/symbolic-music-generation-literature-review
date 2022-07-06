# Automatic Generation of Music for Inducing Emotive Response

## Brief overall summary
### Aim
This research aimed to develop a method for generating music with a chosen emotional content, using statistical models created from a corpus of songs which envoke particular emotions.

### Implementation/Method used
MIDI was used as the symbolic representation of music.
Melodies are generated using n-gram models, representing pitch intervals typically found in the corpus for the chosen emotion.
Harmony is generated using hidden markov models, generating similar harmony to the corous for the chosen emotion.
Accompaniment and instrumentation are also chosen depending on what is most likely found in the relevant corpus.

### Achievements
- Target six basic emotions: love, joy, surprise, anger, sadness, fear.

### Limitations
- Lack of novelty in generated music, sound very similar to eachother.
- No sound examples available for me to listen and tell what kind of accompaniment and instrumentation was generated.