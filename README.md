# Speech2Face
> This project implements a framework to convert speech to facial features as described in the CVPR 2019 paper - [Speech2Face: Learning the Face Behind a Voice](https://arxiv.org/pdf/1905.09773.pdf) by MIT CSAIL group.

A detailed report on results can be found here as [report.pdf](/results/report.pdf). It was made as the final project for CS 753 - **Automatic Speech Recognition** course in Autumn 2019 at Indian Institute of Technology (IIT) Bombay, India.

## Usage

# Folder structure of the project

Efficient structure to arrange the database (audio and video) and the code for this project to avoid any duplication.

```
.
├── base.py
├── LICENSE
├── logs
│   └── ......
├── model.py
├── models
│   └── final.h5
├── preprocess
│   ├── avspeech_test.csv
│   ├── avspeech_train.csv
│   ├── clean_directory.sh
│   ├── data
│   │   ├── audios/
│   │   ├── audio_spectrograms/
│   │   ├── cropped_frames/
│   │   ├── frames/
│   │   ├── pretrained_model
│   │   │   ├── 20180402-114759
│   │   │   │   └── ......
│   │   │   └── 20180402-114759.zip
│   │   ├── speaker_video_embeddings/
│   │   └── videos/
│   ├── data_download.py
│   ├── facenet
│   ├── prepare_directory.sh
│   ├── speaker.py
│   └── video_generator.py
├── README.md
├── requirements.txt
└── results
    ├── ......
    ├── presentation.pdf
    └── report.pdf
```

# Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

1. Go to preprocess folder and run `prepare_directory.sh` and then download AVSpeech Dataset. Run `data_download.py` file for data download from youtube based on AVSpeech Dataset.
```
cd preprocess/
sh prepare_directory.sh
Download [AVSpeech Dataset](https://looking-to-listen.github.io/avspeech/download.html) in the folder.
python data_download.py --from_id 1 --to_id 4000
```
