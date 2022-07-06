# FIGARO: Generating Symbolic Music with Fine-Grained Artistic Control

## Brief overall summary
### Aim
The aim of the research done in this paper was to create a model/method capable of 'global yet fine-grained' controllable music generation. They aim to have the user provide a high-level guidline for the piece which should be generated.

### Implementation/Method used
Their method is based upon a desciption-to-sequence task. The two descriptions that the extract from the input are fed into a Transformer auto-encoder for reconstruction. REMI+ symbolic music representation (based upon REMI from [[(2020) Pop Music Transformer]]) is used as the input format. The extension to REMI allows for multi-track modelling.

A high-level description is extracted from a sequence and the model reconstructs the sequence from this description. The extraction is done using a 'description function', which takes a single bar as the input and extracts the descriptive featurs of that bar.

 Two description functions are used. One, described as a 'hand-crafted expert description', provides a human-interpretable sequence through a hand-crafter algorithm. The other, known as the 'learned' description, uses representation learning to extract high-fidelity important features of the source sequence. This learned representation part of the model is based upon the VQ-VAE framework.
 
 The 'expert' description includes information such as: time signature (one per bar), note density (number of note onsets per quater note), mean pitch, mean velocity, mean duration (average duration of all notes with onsets in the current bar), instruments (list of all instruments that have note onsets in the current bar) and chords (list of all chords being played during the current bar). Chords are extracted using an adapted version of the Viterbi algorithm, also used in [[(2020) Pop Music Transformer]].

### Achievements
- With fine-grained control, as opposed to global control, the control attributes can be arbitrarily varied over time. This could allow for more realistic music generation, as not all high-level features are fixed throughout a music piece.

### Limitations
- 