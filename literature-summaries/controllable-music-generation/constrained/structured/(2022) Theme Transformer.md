# Theme Transformer: Symbolic Music Generation with Theme-Conditioned Transformer

## Brief overall summary
### Aim
The aim of the research done in this paper was to generate symbolic music which is able to repeat, with slight development/variation, a user-given theme.

### Implementation/Method used
In order to extract thematic materials from music pieces, as part of a method to get training data, they used contrastive learning with musically-inspired data augmentation and DBSCAN clustering.

The Theme transformer model is based off of an encoder-decoder transformer model. However, they use a novel gated parallel attention module and theme-aligned positional encoding to refer to the thematic aterial given as a condition.


### Achievements
- Deep learning-based approach, using contrastive representation learning and clustering, to automatically retreive thematic materials from music pieces.
- Novel gated parallel attention module used for a seq2seq encoder-decoder architecture.

### Limitations
- Currently can only be conditioned on one single theme. Music typically has mutliple themes that occur, repeat and are developed throughout.
- Only works with themes extracted from existing music, not yet made to work with user-created themes.
- Could be improve with controllability over how much development/variation is applied to the theme by the model. Authors hint at contrastive learning being applicable in terms of how the generated music "departs from" and "returns to" the theme in the piece.