# Off the Beaten Track: Using Deep Learning to Interpolate Between Music Genres

## Brief overall summary
### Aim
This research aimed to create a tool, of use to EDM DJs, which could interpolate between drum beats. Analogies were draw to the use of crossfade transitions in EDM music that DJs often employ.

### Implementation/Method used
Transitions between different genres of EDM drum beats were acheived using interpolations in the latent space of a VAE and also a GAN (both separated tried).

### Achievements
- Subjective evaluation of the tool with practitioners in the field showed that it could be of use.

### Limitations
- Users rated the interpolations poorly for factors such as its human-like sound. Possibly this is due to no inclusion of dynamics.
- Only drums were involved, this could be extended to multiple instruments.
- Interpolations in latent space only provide novel music as transitions between selected tracks which are in the dataset, in this paper transitions are done between different genres. Possibly a more useful tool would take the users original track/idea for a track and allow them to traverse the latent space in a meaningful way to adjust features of the track.