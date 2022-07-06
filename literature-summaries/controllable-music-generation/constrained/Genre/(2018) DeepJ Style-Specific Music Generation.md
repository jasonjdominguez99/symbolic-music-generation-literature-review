# DeepJ: Style-Specific Music Generation

## Brief overall summary
### Aim
The research in the paper was aimed at creating a model which could be trained on a range of styles/genres and generate music in a particular style/genre as conditioned by the user.

### Implementation/Method used
The model DeepJ is based upon a biaxial LSTM (influenced by [[(2017) Generating Polyphonic Music Using Tied Parallel Networks]]) with the addition of style embedding vectors to condition the model on style/genre of the music, enabling it to generate a specfic style/genre (of baroque, classical or romantic).

Data representation was important for this work. Style was incorporated via one-vectors for each composer in the dataset. A genre was then conditioned at generation time via a style vector with an equal proportion of 1 in each of the position corresponding to composers of that style. E.g. [0.25, 0.25, 0.25, 0.25, 0, 0, 0, ...], where the first 4 elements represent composer of the chosen style with their one-hot vectors being [1, 0, 0, 0, 0, ...], [0, 1, 0, 0, 0, 0, ...], and so on. Dynamics were also modelled by using a matrix of volume values corresponding to a given not, scaled between 0 and 1.

### Achievements
- Subjectively generated music was preferred to that from Biaxial LSTM ([[(2017) Generating Polyphonic Music Using Tied Parallel Networks]]).
- Subjectively, no statistically significant difference between musicians being able to tell the genre of DeepJ's music and real music of the genre. This shows the model achieved its aim of a single model being able to be conditioned for specific genre/style generation.
- Solved style inconsistancies present in Biaxial LSTM work ([[(2017) Generating Polyphonic Music Using Tied Parallel Networks]]).
- I believe the conditioning also works for more custom generation than genre. For example rather than using [0.25, 0.25, 0.25, 0.25, 0, 0, 0, ...], some composer style preference could be used [0.5, 0.2, 0.2, 0.1, 0, 0, 0, ...], or purely generate music of a single composer's style [0, 1, 0, 0, 0, 0, ...].
- Successful modelling of some dynamics which could explain subjective preferences for this model's music over others.

### Limitations
- Music lacks, structure, direction, theme, motifs etc.
- Abrupt start and end.
- Although dynamics was learned as a genre-specific attribute, users have no control over it other than the genre they chose might be more likely to have certain dynamically features.
- Rythmnically limited due to quantization to 16 time steps per bar. Sounds more robotic than real.
- Subject to my thought on the last bullet point in achievements. This conditioning beyond genre is not shown and it is not obvious whether music conditioned purely for the style of a specific composer would be novel sounding or too similar to training data for that composer.
- Representation of music used is "expensive to train". Researchers suggest developing a sparse representation of music to improve upon this.