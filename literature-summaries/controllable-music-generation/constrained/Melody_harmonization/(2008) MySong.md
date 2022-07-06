# MySong: Automatic Accompaniment Generation for Vocal Melodies

## Brief overall summary
### Aim
The aim of this research was to generate chords for  user given vocal melody recording. This is intended for non-musicians to be intuative.

### Implementation/Method used
The algorithm in this paper used a Hidden Markov Model (HHM) to generate chords from the input recording. This was then given to a commercial pattern-based accompaniment software, in order to give the output music of the system a more musical sound.

### Achievements
- User interaction in selecting accompaniment, using sliders for 'jazz factor' and 'happy factor'. Low 'jazz factor' essentially referes to using common chord progressions, whereas increasing 'jazz factor' results in the use of more 'adventurous' chord patterns.
- Controllable tempo of output.

### Limitations
- Songs in the database with mutliple keys separated and treated as separate songs. So no learning of key changes.
- Major, minor, diminished, augmented and suspended traids used. No complex/entended chords included. This does not ruin the harmonization, but can make it less interesting.
- Seems to be one chord per measure/bar.