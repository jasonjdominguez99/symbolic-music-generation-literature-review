# FUNCTION- AND RHYTHM-AWARE MELODY HARMONIZATION BASED ON TREE-STRUCTURED PARSING AND SPLIT-MERGE SAMPLING OF CHORD SEQUENCES

## Brief overall summary
### Aim
The aim of this research was to create a model capable of generating a sequence of chords for a given sequence of musical notes (a melody). It also aims to address the limitations of HMM-based melody harmonization, in that it ignores the hierarchical structure of chords and their harmonic functions (tonic, dominant, subdominant, etc.) and that there is no chord rhythm, only generating a single chord per bar.

### Implementation/Method used
This research developed a hierarchical model, consisting of a probabilistic context-free grammar (PCFG) which generates chord symbols, a metrical Markov model, which generates chord rhythms, and a Markov model which generates a melody from a chord sequence. (This is confusing, because the paper sounded like it was about harmonizing a given melody, but this description of the model makes it sound like a melody is generated, after a chord progression is generated?)

### Achievements
- Results not restricted to a single chord per bar.

### Limitations
- Model favoured choosing simpler, basic chord progressions.
- Number of generated chords tends to be less than the number of bars/measures. Althogether rhythms sound a little out of place, in my opinion.
- No control over the style of chord progression, just whatever fits.
