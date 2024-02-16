# Real-Time Face Recognition with OpenCV and Python

This is a Python script for real-time face recognition using OpenCV and scikit-learn's KNeighborsClassifier. It allows you to collect training data for multiple persons, train a classifier, and then recognize faces in real-time using a webcam.

## Requirements

- Python 3.x
- OpenCV (`pip install opencv-python`)
- NumPy (`pip install numpy`)
- scikit-learn (`pip install scikit-learn`)

## Usage

1. Clone the repository or download the script.
2. Install the required dependencies.
3. Run the script by executing `python face_recognition.py`.
4. Follow the instructions to input the number of persons and their names for training.
5. The script will open your webcam to collect training data. Press 'q' to stop collecting data.
6. Once training data is collected, the script will train the classifier.
7. After training, the script will start recognizing faces in real-time. Press 'q' to quit.

## Files

- `face_recognition.py`: Main Python script.
- `haarcascade_frontalface_default.xml`: Haar cascade classifier for face detection.
- `datas/`: Directory to store training data.
  - `names.pkl`: Pickled file containing labels (names) of the persons.
  - `faces_data.pkl`: Pickled file containing training data.

## Functions

### `collect_training_data(video_capture, faces_detector, name, max_samples=100)`

Collects training data for a specific person.

- `video_capture`: OpenCV VideoCapture object.
- `faces_detector`: OpenCV CascadeClassifier for face detection.
- `name`: Name of the person for whom data is being collected.
- `max_samples`: Maximum number of training samples to collect (default is 100).

### `recognize_faces(video_capture, faces_detector, knn_classifier)`

Recognizes faces in real-time using a trained classifier.

- `video_capture`: OpenCV VideoCapture object.
- `faces_detector`: OpenCV CascadeClassifier for face detection.
- `knn_classifier`: Trained scikit-learn KNeighborsClassifier.

### `main()`

Main function to execute the script.

## Credits

This script is inspired by various tutorials and examples available online for face recognition using OpenCV and scikit-learn.

