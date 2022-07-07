# Chord Generation From Symboloic Melody Using BLSTM Networks

## Brief overall summary
### Aim
The aim of this research was to solve to task of melody harmonization, using a symbolic approach.

### Implementation/Method used
The model developed in this paper is based on a bidirectional LSTM (BLSTM).

### Achievements
- 23.8% and 11.4% increased performance when compared to HMM and DNN-HMM respectively. (Unsure what is quantified as performance increase, but it seems like objective not subjective evaluation).
- Different time signatures are handled by normalizing note durations by multiplying them with the reciprocal of the time signature.

### Limitations
- Only major and minor triad chords considered. More complex chords not considered.
- Only one chord per bar. Data was preprocessed to only take the first chord in a bar.
- Only songs in major key were considered.
- The notes of each bar are stored in a vector of 12 semitone classes. I believe that, in doing this, temporal information within a bar is lost.