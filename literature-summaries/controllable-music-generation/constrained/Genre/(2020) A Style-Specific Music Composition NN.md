# A Style-Specific Music Composition Neural Network

## Brief overall summary
### Aim
The research in this paper aimed to improve upon existing symbolic music generation techniques with respect to the structure of generated pieces. This was 'style-specific' music generation, depending on the style of music the mode was trained on. From what I can understand (the paper is not easilt understood in my opinion) the model generates classical music (possibly piano pieces only, however multi-track is mentioned?).

### Implementation/Method used
The model in this paper is a hybrid of an LSTM, for the sequence generation portion of the music generation task, and reinforcement learning, in the for of and actor-critic (AC) network, to constrain generation with respect to theorectical music rules.

### Achievements
- Reinforcement learning used to mitigate the tendancy of GANs to generate similar examples.

### Limitations
- It is unclear, but other genres are mentioned, including pop, with examples of generated music given. In particular a pop music piece had a quite realistic and music drum part, but it is not clear if drums were included as part of the model or if this was added to put the generated piano part in context. What is clear is that the model individually targets a specific style and a sigle model cannot be controlled by the user to generate music of a chosen style.
- 30% of users said the generated music can meet 'actual requirements for style music'. (Not sure what this means, this paper is full of poor english leading to ambiguous sentences)
- Besides training the model on a dataset of music of your chosen genre/style, there is no control over the generated music. Not very useful.