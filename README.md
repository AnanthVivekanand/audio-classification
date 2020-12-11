# Audio Classification

## Project Description

This project was created for the Independent Study and Mentorship program. The ISM program allows Frisco ISD students 
to explore interested fields through research and mentorship, developing life-long skills in the process. Students 
showcase their knowledge through the semester-long projects known as the Original Work and Final Product. Furthermore, students acquire mentorship from
professionals, developing communication and valuable connections.

This year in ISM, I am exploring the field of Machine Learning with a special focus on audio classification. This 
repository documents my code for my Original Work and provides an easy-to-use UI for navigating through my code.

## Quick Links

* [Commits](https://github.com/AnanthVivekanand/audio-classification/commits): Documentation of my work over time in the form of incremental updates.
* [Digital Portfolio](http://ananthvivekanand.weebly.com): My digital portfolio showcasing my work in ISM.

## Getting started

This guide assumes you have basic familiarity with the terminal. 

1. Open a terminal environment. 
1. Clone this repository: `git clone https://github.com/AnanthVivekanand/audio-classification.git`
2. Navigate into the `GUI/` directory: `cd audio-classification/GUI/`
3. Install all python dependencies: `pip3 install -r requirements.txt`
4. Then run `application.py`: `python3 ./application.py`
5. Navigate to `http://localhost:5000/` in your web browser

Documentation:

* [`GUI/application.py`](GUI/application.py): This is a simple [Flask application](https://flask.palletsprojects.com/en/1.1.x/) that creates a HTTP API for the audio classification model. 
* [`GUI/templates/home.html`](GUI/templates/home.html): This is the front-end HTML code that the provides a file upload and visualization interface.
* [`final_model/weights.h5`](final_model/weights.h5): This binary file contains the "weights" of the trained machine learning model. 
* [`preprocessing/extract_fft_data.ipynb`](preprocessing/extract_fft_data.ipynb): This file extracts Short-time Fourier Transform data from .wav files in the dataset. This allows for faster training as the STFT is computed only once and stored indefinetely.
* [`training/optimized_TCN.ipynb`](training/optimized_TCN.ipynb): This file implements a Temporal Convolutional Neural Network that classifies STFT inputs into one of 10 catagories. This is the model that the Flask application uses.

Acknowledgements:

* Dr. Abhishek Sehgal at Samsung Research America
* Mr. Gautum Bhat at UTD's Statistical Signal Processing Research Laboratory
