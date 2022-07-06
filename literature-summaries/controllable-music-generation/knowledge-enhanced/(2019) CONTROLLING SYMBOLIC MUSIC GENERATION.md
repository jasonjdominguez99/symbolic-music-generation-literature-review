# CONTROLLING SYMBOLIC MUSIC GENERATION BASED ON CONCEPT LEARNING FROM DOMAIN KNOWLEDGE

## Brief overall summary
### Aim
The aim of the research done in this paper was to approximate musical domain knowledge via a function and use this to create a generative model with a latent spaces that captures musical concepts, such as rhythm, contour (how music moves between the notes) and fragmentation & consolidation (F&C), in order to conrtol the generation of music. Each decoupled latent space is associated with a musical concept, therefore the are refered to as 'latent-space concept'. 

### Implementation/Method used
Knowledge is incorporated into this model via funtion approximations. These functions are said to approximate musical concepts including rhythm, contour and F&C. The writers say that these concepts can be approximated from an input sequence with rules or algorithms, in order to construct the functions.

Control can be achieved via two methods: concept-axes interpolation and concept-aware variation generation.

### Achievements
- 

### Limitations
- Only uses 4/4 meter music
- Domain knowledge used for musical concepts, but these conceots, e.g. rhythm and contour, are pretty low level.
- Monophonic melodies only, no polyphony or multi-track, therefore no harmony.
- 