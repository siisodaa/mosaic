Overview:
---------
This script generates a mosaic image from a pool of images. It matches small sections of a target input image with the most similar images from the pool based on average color, assembling a larger mosaic image as the output.

Requirements:
-------------
- Python 3.x
- numpy
- opencv-python
- tqdm

The required Python packages can be installed using the following command:
pip install -r requirements.txt

Setup:
------
1. Clone or download this repository to your local machine.
2. Ensure that you have Python 3.x installed.
3. Install the required dependencies as listed in the 'requirements.txt' file.

File and Folder Structure:
--------------------------
- data/input.jpg: Default path for the input image. Replace 'input.jpg' with your target image for the mosaic.
- data/output.jpg: Default path where the mosaic image will be saved. You can change this path in the script as needed.
- jds/: Folder containing the pool of images used to create the mosaic. Place all potential mosaic pieces in this folder.

Usage:
------
1. Update the 'Options' class in the script to point to the correct paths for your input image, output image, and image pool.
2. Adjust the 'stride' parameter in the 'Options' class if necessary. This parameter affects the granularity of the mosaic tiles.
3. Run the script using a Python interpreter. For example:
   python mosaic_generator.py

This will generate the mosaic image and save it to the specified output path.

Configuration:
--------------
The script includes several configurable options within the 'Options' class:
- input_path: Path to the input image.
- output_path: Path where the output image will be saved.
- pool_path: Path to the folder containing the pool of images.
- stride: Controls the size of each mosaic tile; smaller values increase the resolution of the mosaic but require more images.

Notes:
------
- Ensure the 'jds' folder has a sufficient number of images to fully cover the mosaic. The script checks the availability of images and will notify if there are not enough.
- The progress of the mosaic generation is displayed via a progress bar using 'tqdm'.

For further adjustments or custom configurations, modify the script as needed to suit your specific requirements.
