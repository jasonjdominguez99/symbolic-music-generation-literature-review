# Learning Interpretable Representation for Controllable Polyphonic Music Generation

## Brief overall summary
### Aim
The aim of the research done in this paper was to create a model capable of being controlled for chord and texture, by using inductive biases in the model to create chord-texture disentanglement.

### Implementation/Method used
The model that was created works with 8-beat/2-bar polyphonic music pieces. The model is an adaptation of a conditional VAE. There are two encoder, one for chords and one for texture. 

The chord progression is extracted from the input using algorithmic methods, fed into a bi-directional GRU and encoded to a latent space vector. The representation of chord here consists of a one-hot vector for the root, a one-hot vector for the bass and a multi-hot vector for chroma. The chord progression is then reconstructied via a GRU-based decoder.

The second decoder, which deals with texture, takes in a image-like form of the music, similar to piano-roll. This is fed into a CNN. The researchers propose that the translational invariance of convolution layers and the blurriness of pooling layers helps the model capture a chord-invariant representation of texture. The output of the CNN is then passed to a bi-directional GRU and encoded to a latent space vector. The main decoder of this model is based upon PianoTree VAE [[(2020) PIANOTREE VAE]] and it takes in the concatenated chord latent vector and texture latent vector.

### Achievements
- Texture and chord disentanglement shown to have been achieved via augmented data with changes in pitch resulting in larger changes in chord latent code than texure and similarly for rhythm influencing texture more than chord.
- Compositional style transfer shown, with swapping the texture representations of pieces, or the chord representations and the generated piece maintaining rhythm or pitch with the pitch or rhythm of the different piece, respectively.
- Accompaniment generation is achieved by strapping on the EC$^{2}$-VAE from [[(2019) DEEP MUSIC ANALOGY]] to generate a melody, upon which the generation is conditioned. It is also conditioned on two bars of true accompaniment and the generated accompaniment shows repeating bass notes and rhythmic patterns from the condition.

### Limitations
- Only 2/4 and 4/4 meter music used.
- Texture variation by sampling not really very interpretable or useful. More like randomly changing things. Although chords remain the same, as intended, the left hand piano part remains mostly the same, with a different improvised melody over the top. This isn't what I would expect from textural change, I'd expect more rhythm change with the melody similar, but rhythmically different perhaps.
- Would be better if you could change the texture to be more sparse, or most something... rather than aimlessly resampling.