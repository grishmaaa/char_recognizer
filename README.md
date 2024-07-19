# Character Recognizer

This project is a character recognition system that uses OpenCV and K-Nearest Neighbors (KNN) for recognizing handwritten characters. The project consists of two main scripts: `main.py` for training the model and `t&t.py` for testing the model.

## Project Structure

- `main.py`: Script to train the character recognition model.
- `t&t.py`: Script to test the character recognition model.
- `classifications.txt`: File containing classifications of the training characters.
- `flattened_images.txt`: File containing flattened images of the training characters.
- `training_chars.png`: Image file containing characters for training.
- `test1.png`, `test2.png`, `test3.png`: Image files for testing the character recognition model.

## Requirements

- Python 3.x
- OpenCV
- NumPy

## Installation

1. Clone the repository or download the project files.
2. Install the required Python libraries using pip:
    ```bash
    pip install opencv-python numpy
    ```

## Training the Model

1. Prepare an image file (`training_chars.png`) containing the characters you want to train the model with.
2. Run the `main.py` script to train the model:
    ```bash
    python main.py
    ```
3. The script will process the training image and create `classifications.txt` and `flattened_images.txt` files.

### Running `main.py`

The `main.py` script reads the training image, processes it to find contours, and asks the user to input the character for each contour. It then saves the classifications and flattened images to text files.

Usage:
```bash
python main.py
```

### Important Points:

- The script displays each detected character one by one and waits for the user to input the corresponding character from the keyboard.
- Press `ESC` to exit the program.
- Only valid characters (0-9, A-Z) are accepted.

## Testing the Model

1. Prepare an image file (`test1.png`, `test2.png`, `test3.png`) containing the characters you want to recognize.
2. Run the `t&t.py` script to test the model:
    ```bash
    python t&t.py
    ```

### Running `t&t.py`

The `t&t.py` script reads the test image, processes it to find contours, and uses the trained KNN model to recognize each character. It displays the recognized characters and draws rectangles around them on the test image.

Usage:
```bash
python t&t.py
```

### Important Points:

- The script displays the test image with rectangles drawn around the detected characters.
- It also prints the recognized characters to the console.

## Sample Data

- `training_chars.png`: Image containing training characters.
- `test1.png`, `test2.png`, `test3.png`: Sample images for testing the recognition model.

## Notes

- Ensure the training and testing images are preprocessed properly (grayscale, blurred, thresholded) for better recognition accuracy.
- Adjust the contour area threshold (`MIN_CONTOUR_AREA`) as needed for your specific use case.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any improvements or bug fixes.

## License

This project is licensed under the MIT License.
