# Computer-Generated Music for Tabletop Role-Playing Games

## Brief overall summary
### Aim
This research aimed to create a model for generating background music for D&D, based on the storyline, i.e. using player's voice as contextual input.

### Implementation/Method used
Emotion was classsified from user audio using a fine-tuned BERT language model. With this classification of emotion, music was generated using a 'Stochastic bi-objective search algorithm', the researchers' adaptaion of a stochastic beam search algorithm. They represent emotion using valence-arousal pairs (as explained in [[(2021) Learning to Generate Music with Sentiment]]). I believe music was symbolically represented.

### Achievements
- General subjective agreement that the generated music represent the desired emotions. Participants identified the emoition of generated pieces as often as they did with real music.
- Real-time music generation to keep up with the game.

### Limitations
- After listening to examples, transitions are very abrupt.
- Generated music is only for polyphonic piano.
- Application is a bit abstract from helpful tools for composers.