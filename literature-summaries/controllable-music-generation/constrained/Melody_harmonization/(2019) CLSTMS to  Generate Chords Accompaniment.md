# CLSTMS: A Combination of Two LSTM Models to Generate Chords Accompaniment for Symbolic Melody

## Brief overall summary
### Aim
This research aimed to tackle the task of melody harmonization. The developed model (CLSTMS) takes in a melody and provides a chord for each measure of the melody.

### Implementation/Method used
The model developed in this paper uses two LSTM models. One deals with the relationship between melody notes, grouped by measure, and the chords and the other deals with 'chord transfer rules'.

### Achievements
- Performs better than hidden Markov models (HMMs)

### Limitations
- Only triads chords used, including: major, minor, diminished, augmented and suspended.
- Does not allow multiple chords per measure.
- Rhythm not including. Only predicts a chord for a bar.