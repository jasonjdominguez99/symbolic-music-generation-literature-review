# Mind Band: A Crossmedia AI Music Composing Platform

## Brief overall summary
### Aim
The research aimed to create an app/web interface, with which users could upload an emoji, picture or audio clip of them humming (not clear if it has to be humming or not) and retrieve AI-generated music with similar VA (valence-arousal) values.

### Implementation/Method used
A VAE-GAN model was used to generate thousands of music pieces. These were then used to populated a database of music examples. The clips were then mapped to VA values using OpenSmile and JSymbolic2. User inputted emojis, pictures or audio clips are then equivalently mapped to VA values. From this, a music clip in the database, which has a similar VA value, is selected.

### Achievements
- Generated music is multi-track.

### Limitations
- Composition of generated music is not really conditioned on emotion. Rather, many music clips are generated, with random emotional value, and then categorized based on their emotional value (or specifically VA values).
- A more sofisticated system would extract the sentiment of the user's input and then use that to condition a generative model, creating new music in real-time (the writer's allude to something similar as being a possible improvement).