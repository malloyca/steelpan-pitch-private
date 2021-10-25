# Roadmap Steelpan-pitch

Steelpan-pitch is a research project investigating various methods for performing pitch detection on steelpan audio signals.


## SASS-E (Steelpan Analysis Sample Set for Evaluation)

This is my steelpan audio dataset for analysis.

### Tasks
- Create Python script for quick mass editing of samples (trim to approx -60 dBFS based on power levels)
- Edit samples for Wabich lead (or whichever pan it is)
- Future tasks:
  - Record samples for other mallets (rods, chopsticks, cardboard tubes, etc)
  - Record samples my collection of double tenors and double seconds (after tuning?)
  - Host on Zenodo


## Steelpan-crepe

This portion of the project is to investigate the use of Crépe and Crépe-like convolutional neural networks.

### Tasks

- Save processed audio files for training/validation (as `*.npy` arrays?) so we don't have to process all of the audio every time we run the script?
- Re-training
  - Batch size
    - 32
    - 64
    - 128
    - 256
    - 512
  - Clean up metrics
  - Callbacks
    - Early stopping based on validation accuracy
    - Checkpoints
  - Clean up notebook to make it more presentable
    - Add documentation
    - Add commentary
    - Delete notes
    - Complete todos
      - Check `db_to_pow` function / compare with Librosa's
      - Delete cell testing `db_to_pow`
      - Refine `load_audio_batch` function
      - Figure out bettern name for `load_audio_batch`
      - Can we use Numba to speed up `load_audio_batch`?
      - Clean up `load_audio_batch` documentation
      - Check early stopping comparator (set to minimize)
      - Set save_weights_only to False (save whole model)
      - Make sure callbacks are working
  - Redo do training data result visualizations
- Training Crepe network from scratch
  - Create a notebook for this
- Modifications to Crepe
  - Reduce output space to constrain to tenor steelpan range +/- 40 cents
  - 



## Audio feature extraction + neural networks

This portion of the project is to investigate the use of audio feature extraction (via Essentia) and
neural networks as a method for pitch detection on steelpan audio signal.

### Tasks
- Select audio features to use
  - 
- Write Python script to perform audio feature extraction
- Determine which audio features help and which do not
- Determine optimal neural network architecture
  - Traditional DNN
    - Sigmoid output layer vs softmax?
    - How many output neurons per semitone?
- 


## Realtime pitch detection

It is important to find computationally efficient methods of steelpan pitch detection in order to allow their use in live intelligent audio processing.

This will get more development soon. The current plan is to implement this as a VST using MATLAB's audio and machine learning toolboxes.

### Tasks
- Get started
