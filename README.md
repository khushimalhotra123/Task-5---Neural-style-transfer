# Neural Style Transfer

This project implements Neural Style Transfer, a technique that allows you to combine the content of one image with the artistic style of another. The result is a new image that preserves the content of the original image while adopting the style of the other image, creating stunning visual effects.

## Table of Contents

- [Introduction](#introduction)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction

Neural Style Transfer uses a convolutional neural network (CNN) to blend the content of a content image with the style of a style image. The technique was first introduced by Gatys et al. in their 2015 paper, "A Neural Algorithm of Artistic Style."

## How It Works

The core idea behind Neural Style Transfer is to optimize an image such that it simultaneously minimizes the difference between:
- The content representation of the content image.
- The style representation of the style image.

The optimization process involves:
1. Extracting the content and style features using a pre-trained CNN (e.g., VGG19).
2. Defining a loss function that measures the difference between the generated image's content and style features and the corresponding features from the content and style images.
3. Iteratively updating the generated image to minimize the loss.

### Key Components:
- **Content Loss**: Captures the difference between the content features of the generated image and the content image.
- **Style Loss**: Captures the difference between the style features of the generated image and the style image.
- **Total Variation Loss (Optional)**: Regularizes the generated image to reduce noise.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/neural-style-transfer.git
    cd neural-style-transfer
    ```

2. **Set up a virtual environment (optional but recommended):**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare your images:**
   - Place your content image and style image in the `images/` directory.

2. **Run the script:**
   ```bash
   python neural_style_transfer.py --content_path images/content.jpg --style_path images/style.jpg --output_path results/output.jpg
   ```

3. **Adjust hyperparameters:**
   - You can tweak the content and style weights, learning rate, and number of iterations by passing additional arguments:
   ```bash
   python neural_style_transfer.py --content_weight 1e3 --style_weight 1e-2 --num_iterations 1000
   ```

4. **View the result:**
   - The generated image will be saved in the `results/` directory.

## Contributing

Contributions are welcome! If you have ideas for improvements or new features, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
