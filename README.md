# JazzAI
Automatic analysis of jazz solos to help jazz players improve their playing

## User experience
- User wants to improve their jazz playing to sound more like a pro
- They record themselves playing a jazz solo 
- They input their playing into the JazzAI program
- The user is presented with an analysis of their playing
-   Artists they resemble
-   Parts that sound good/bad
-   Ideas on how to improve their soloing/what is missing from their playing

## How it could work
- Train an AI on a dataset of jazz playing so that it can identify jazz solos of particular artists
- Model should output the likelihood that a section of audio belongs to a jazz solo or is from a particular artist
- These likelihoods could be presented in way to show what parts of player's own solos resemble actual jazz playing and what don't
- Could use generative AI or some sort of diffusion method to make the player's solo approximate an artist's solo, and use this transformation information to present improvement data to the player
## Milestones
- [ ] figure out how to use WSL2 with github
- [?] use [basic pitch](https://huggingface.co/spotify/basic-pitch) or demucs to separate out the saxophone from a jazz song (done (poorly) but need to upload code to the github)
- 

## Current tasks
- Compile the literature on
  - existing music transcription software/projects
  - existing jazz analysis AI projects
  - helpful tools
- Devise a basic architecture/pipeline for the project


Things to learn
- What is a U-net convolutional architecture (used by Demucs)
