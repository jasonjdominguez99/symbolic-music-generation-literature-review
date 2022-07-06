# Pop Music Generation: From Melody to Multi-style Arrangement

## Brief overall summary
### Aim
This research aimed to solve the issue of music generation with a particular style, for mutli-instruement arrangments. They do this with an end-to-end multi-track music generation system for melody and arrangement.

### Implementation/Method used
A melody is generated using a chord progression as a guide. Song generation then uses a rhythm and melody cross-generation method. A multi-task joint generation network is then used for the generation of arrangement.

Music style is controlled using a reinforcement learning adversarial approach. 

### Achievements
- Harmony achieved over multiple tracks
- Subjectively better results than other models
- Quantifiable evidence (possibly subjective, I can't tell) for the use of multiple disciminators in addition to models to improve 'harmony score'. Shows multi-task learning improved performance. Multiple discriminators (reinforcement learning) also used to influence style.

### Limitations
- Limit of musical styles (classical, pop and jazz only)
- Data driven
- Instruments not chosen automatically
- Emotion not considered
- Length limitations
- Limited choice of instruements within a set style. Cannot choose 3 guitar tracks, 1 drum, 1 bass for rock. Only taken to be what the researchers found was the average for the style.