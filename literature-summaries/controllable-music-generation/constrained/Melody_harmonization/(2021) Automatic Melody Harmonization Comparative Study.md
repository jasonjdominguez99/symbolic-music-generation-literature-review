# Automatic Melody Harmonization with Triad Chords: A Comparative Study

## Brief overall summary
### Aim
This was a comparative study of several different techniques used for the task of melody harmonization. Both subjective and objective evaluation was done.

### Implementation/Method used
Five melody harmonization models were used, including: template matching, hidden Markov models (HMMs), genetic algorithms (GAs) and two variants of deep learning recurrent neural networks (RNNs). Six objective metrics used, as well as a subjective evaluation.

### Outcomes of comparisions
The researchers concluded that deep learning methods out performed non deep learning model in harmonicity and interestingness.
They note that future work in the area could include: extended the chord vocabulary to more complex chords and transformer-based models for increased structure/time dependance.

### Limitations of comparisons
- Dataset consisted of alter/simpler chords in order to reduce task difficulty.
- Triad chords only.
- No performance, such as velocity or rhythm.
- Full potential of all models for melody harmonization task was not explored. For example, trying to introduce some harmony term into the loss function.