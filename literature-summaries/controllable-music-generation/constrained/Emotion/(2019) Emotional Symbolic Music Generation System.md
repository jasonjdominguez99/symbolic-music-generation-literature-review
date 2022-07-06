# An Emotional Symbolic Music Generation System based on LSTM Networks

## Brief overall summary
### Aim
This research in this papers aimed to create a model capable of generating novel music, conditioned on its emotional content, as indicated by a valence-arousal (VA) value.

### Implementation/Method used
The model generated used a BALSTM with lookback to generate the music, which was trained on a dataset of MIDI piano parts.

### Achievements
- Generated music was polyphonic.
- In subjective evaluation, 72% classification accuracy was achieved for happy generated pieces.

### Limitations
- Only single, polyphonic piano parts were generated, not multi-track/multi-instrument.
- In subjective evaluation, 60% or less (around 50%) classification accuracy was achieved for sad, peaceful and tensional generated pieces.
- Range of emotional able to be conditioned seems small, just happy, sad, peaceful and tensional.
- Music restricted to 4/4 time signature and 16 beats per bar. Rhythmnic limtations could affect perceived emotion.