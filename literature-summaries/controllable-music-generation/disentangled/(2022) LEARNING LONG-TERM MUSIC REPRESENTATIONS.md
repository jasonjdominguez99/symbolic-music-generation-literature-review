# LEARNING LONG-TERM MUSIC REPRESENTATIONS VIA HIERARCHICAL CONTEXTUAL CONSTRAINTS

## Brief overall summary
### Aim
The aim of the research done in this paper was to improve upon the work done in [[(2019) DEEP MUSIC ANALOGY]], to allow for longer (eight-bar) music phrases, when compared to the two-bar phrases able to be generated/manipulated with EC$^{2}$-VAE. 

### Implementation/Method used
The approach used is built upon the EC$^{2}$-VAE model from [[(2019) DEEP MUSIC ANALOGY]].  Their method has two stages: pre-training and fine-tuning.

Pre-training invloves training the  EC$^{2}$-VAE model to learn a short-term representation, which is disentangled between rhythm and pitch. A second model for long term structure, called Long-EC$^{2}$-VAE, is then trained using NCE-based contrastive loss (contrastive learning) with the short-term model, so as to not deviate too far from the well-learned short-term music representations.

In fine-tuning, a hierarchical model is created by using the Long-EC$^{2}$-VAE encoder with a hierarchical decoder. This is trained in two steps. First, the decoder is trained, with the endoder fixed, andthen the model is trained as a whole. This is said to be to improve the rhythm-pitch disentanglement.

### Achievements
- Novel use of Structured InfoNCE loss to perform contrastive learning and stablize long-term model training.
- Eight-bar controllable symbolic music manipulation, including: generating a melody with the pitch of one melody and the rhythm of another (due to mixing the disentangled rhythm-pitch representations), disentangled interpolations between melodies (example shown goes from rhythm of one melody, closer to the rhythm of another, whilst maintaining pitch info)

### Limitations
- Only monophonic melody control achieved, could be extended to melody harmonization, or multi-track, with rhythmic control over chords for example.
- Control over any other attributes, or composite attributes, such as emotion, would require retraining and model resign for disentanglement between the different attributes.
- Although refered to as 'long-term' structure, eight bars represents at most one section of an entire musical piece, so there is no work on overall musical piece structure or direction such as a verse-chorus transition in a pop song, or a build up to a climactic section.
- Attribute control is relatively low-level, not high level qualitative control like emotion or genre/style.