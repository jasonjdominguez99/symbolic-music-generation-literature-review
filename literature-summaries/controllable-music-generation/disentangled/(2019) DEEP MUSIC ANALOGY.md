# DEEP MUSIC ANALOGY VIA LATENT REPRESENTATION DISENTANGLEMENT

## Brief overall summary
### Aim
The aim of the research done in this paper was to create a model capable of finding an explicitly coded disentangled representation of symbolic music, specifically disentangled between pitch and rhythm. Explicitly coded here refers to that fact that the model was design to learn how to disentangle these features, rather than a model whose latent space is traversed after training, to create/find disentanglement.

### Implementation/Method used
They use the idea of generation via analogy (A is to B as C is to D) to control the generative output, which are monophonic melodies, constrained by additional chord input. The model they created, called 'explicitly-constrained conditional variational autoencoder' (EC$^{2}$-VAE), is based on a basic VAE, with a bi-directional GRU melody encoder, with GRU decoder. The novel additions to this model include: splitting the latent code into pitch and rhythm latent vectors, having the an additional decoder fot the rhythm latent code, having a reconstruction loss for the pitch part and one for the output of the rhythm decoder, and using ELBO objective to achieve disentanglement, with minimal reduction in overall reconstruction performance.

### Achievements
- Objective, quantifiable evidence of rhythm-pitch disentanglement. This is shown via f-score and via graphs showing the change in pitch and rhythm when changing a specific part of the latent code.
- Several 'what if' interpolation and swapping examples, from a source melody, to show the control over the generative output, including:
	- Analogy of source's pitch is to source's melody as target's pitch is to ?. I.e changing the pitch latent representation of the source melody, but keeping the rhythm the same, which successfully has the effect of using putchs from a different target melody and rhythm from the source melody, in the generated melody. This was all subject to the same chords. It can have the effect of a key change if the target chords are different from source.
	- The same as above, but keeping the pitch latent code the same as the source melody and getting the rhythm representation from a different target melody. This is very ideal rhythm control, as you can specify a rhythmic guide and it will force the generated melody to that rhythm.
	- Analogy by chord change. Only the chords are changed, leading to a slight change of melody (i.e. not just the same thing transposed) in the target key, even with change from major to minor mode, when appropriate.
	- Smooth interpolations from one melody to another, with clearly separate control/interpolation between pitch and rhythm axes.

### Limitations
- Only monophonic melodies.
- Rhythmic control could be added from chord information, to make model suitable from melody harmonization, adding chords as something to be generated too.
- Only pitch and rhythm control.
- No tempo, meter variation, or control.
- Independent control of pitch and rhythm (as well as possibly other attributes) does not correspond to high-level interpretable control over the output in terms of composites of these low level features, such as happy to sad would mean changing chords/key to minor, changing pitches to accentuate the minor notes, changing rhythm to be more sparse and changing tempo to be slower, for example.
- Only 8-beat/2-bar melodies (however [[(2022) LEARNING LONG-TERM MUSIC REPRESENTATIONS]] extends this)