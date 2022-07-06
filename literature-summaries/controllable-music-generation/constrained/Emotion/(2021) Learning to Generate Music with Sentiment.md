# Learning to Generate Music with Sentiment

## Brief overall summary
### Aim
The aim of this research was to create a model which could be used to both classify the sentiment of a musical piece and to generate musical pieces with a given sentiment. 

### Implementation/Method used
An mLSTM model was used and music was represented in a symbolic format. Sentiment was represented as a two value valence-arousal pair (a commonly used continuous numerical representation that defines how happy or sad (valence) and how intense or calm (arousal) the music is).

### Achievements
- Created the first dataset of symbolic (MIDI) piano pieces with sentiment labels.
- Model outperformed previous attempts at classifying sentiment in music.
- When generating music, subjective assessment of the pieces showed that the majority of listeners agreed that positive (happier) pieces had the desired sentiment.

### Limitations
- Generated negative pieces were more ambiguous, as determined by subjective analysis.
- Only polyphonic piano parts used in this research. So no multiple track/instruments.
- Generating music with given valence-arousal pair is not quite equivalent to emotion.