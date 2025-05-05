Data Augmentation for MiniBAGLS Dataset
This repository contains code for performing data augmentation on the MiniBAGLS dataset. The augmentation is achieved using the Albumentations library, and it includes transformations such as flips, rotations, Gaussian blur, elastic transformations, and brightness/contrast adjustments. The goal is to augment the dataset to increase its diversity and improve the performance of machine learning models for tasks like segmentation.

Requirements
To run the script, you need to have the following Python libraries installed:

numpy

albumentations

opencv-python

matplotlib

You can install these dependencies using pip:

bash
Copy
pip install numpy albumentations opencv-python matplotlib
Usage
Set the Random Seed: The random seed is set based on the matriculation number. Replace matriculation_number with your actual matriculation number to ensure reproducibility of results.

python
Copy
matriculation_number =   # Replace with your actual matriculation number
Path to Dataset: Update the extract_path variable to the path where your MiniBAGLS dataset is stored:

python
Copy
extract_path = '' # Replace it with actual path
Image and Mask Selection: The script will randomly select an image, its corresponding mask, and metadata from the dataset. Ensure that your dataset follows the naming conventions where the images have extensions like .jpg or .png, and the corresponding masks have names like image_name_seg.png.

Augmentations: The script defines a set of augmentations using Albumentations. The following transformations are applied to both the image and the mask:

Horizontal Flip: Flips the image horizontally.

Vertical Flip: Flips the image vertically.

Random Rotate 90°: Randomly rotates the image by 90 degrees.

Gaussian Blur: Applies a Gaussian blur with a random blur limit.

Elastic Transform: Applies an elastic transformation to the image.

Random Brightness Contrast: Randomly adjusts the brightness and contrast of the image.

You can customize the augmentations in the A.Compose() function to include or exclude certain transformations.

Visualize the Results: After the augmentation is applied, the script will visualize the original and augmented image along with the mask. This helps to verify how the augmentations are affecting the dataset.

Example Output
The script displays four images in a 2x2 grid:

Top-left: Original image

Top-right: Original mask

Bottom-left: Augmented image

Bottom-right: Augmented mask

Notes
Make sure that the MiniBAGLS dataset is properly extracted and that the image, mask, and metadata files are in the correct format.

If you encounter any issues with the dataset not being found, double-check the file paths and naming conventions.

License
This repository is licensed under the MIT License. See the LICENSE file for more information.




