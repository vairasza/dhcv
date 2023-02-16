# README

## Purpose
bundles all CV methods for the digital humanities project Distant Viewing of Youtube Game Walkthroughs

## Installation
- create virtual env with Python 3.10.
- activate virtual env for project path.
- use `python -m pip install -r requirements.txt` to install dependencies.
- check if all dependencies are installed by importing dependencies in `all_cv.ipynb`.
- detectron2 must be installed manually. script is in `all_cv.ipynb`.
- following error can be ignored: `ERROR: Cannot install -r requirements.txt (line 40), google-auth==1.4.2 and tensorboard==2.11.2 because these package versions have conflicting dependencies.`

## Changing Dependencies
- pip freeze > requirements.txt

## google drive output path
G:\\My Drive\\digital_humanities\\Ergebnisse

## google drive input path
G:\\My Drive\\digital_humanities\\Walkthroughs

## Running
- configurate in `config.json` which methods and games you want to run
- available methods and games listed here
- 
### methods
  - Location
  - AverageColor
  - ObjectDetection
  - Emotion
  - AgeGender
  - Brightness
  - DominantColor

### games
  - Die_Siedler3
  - Diablo2
  - Elden_Ring
  - Half_Life2
  - Little_Nightmares
  - NFSMW
  - Starcraft2
  - Super_Mario_World

- set `inputRoot` to folder where your raw images are located. can be mounted google drive.
- `inputRoot` requires a folder for each game.
- set `outputRoot` to folder where your generated csv, graphs and images are saved. can be mounted google drive.
- `outputRoot` require a folder for each method which further requires a folder for each game.
- the naming of methods and games must be exactly like mentioned above.
- if you do not want to run object detection, uncomment detectron2 related imports
- code blocks that have `#required` in the first line, must be loaded before `#run` block
- code blocks that have `#optional` in the first line, must be loaded if there methods are configured in `config.json`
- Object Detection requires a GPU