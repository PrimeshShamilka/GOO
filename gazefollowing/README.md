# Gazefollowing

This folder contains the code for implementing, training, and testing of models on the **gaze estimation** task. 

## Baselines

1. A. Recasens*, A. Khosla*, C. Vondrick and A. Torralba. **"Where are they looking?"** 
    * Select by setting --baseline='recasens'
2. Dongze Lian, Zehao Yu, Shenghua Gao. **"Believe It or Not, We Know What You Are Looking at!"**
    * Select by setting --baseline='gazenet'
    
## Usage
Training on GOOSynth:
```
python main.py --baseline='gazenet' \
--train_dir='../goosynth/1person/GazeDatasets/' \
--train_annotation='../goosynth/picklefiles/trainpickle2to19human.pickle' \
--test_dir='../goosynth/test/' \
--test_annotation='../goosynth/picklefiles/testpickle120.pickle' \
--log_file='training.log' \
--save_model_dir='./saved_models/temp/' \
```

To continue training from previous run:
```
python main.py --baseline='gazenet' \
--train_dir='../goosynth/1person/GazeDatasets/' \
--train_annotation='../goosynth/picklefiles/trainpickle2to19human.pickle' \
--test_dir='../goosynth/test/' \
--test_annotation='../goosynth/picklefiles/testpickle120.pickle' \
--log_file='training.log' \
--save_model_dir='./saved_models/temp/' \
--resume_training
--resume_path=
```