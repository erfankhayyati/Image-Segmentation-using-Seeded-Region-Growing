# Image-Segmentation-using-Seeded-Region-Growing
# Benign and Malignant Breast Tumors Segmentation Using Seeded Region Growing

Dataset: MIAS "Mammographic Image Analysis Society" 
Dataset link: http://peipa.essex.ac.uk/info/mias.html

For installing requirements:
pip install -r requirement.txt


Steps:
1. Read Annotations
Load the CSV file into a DataFrame with annotations.

2. Filter Annotated Images
Retain only images with annotations (most images lack annotations).

3. Store Images
Save annotated images to a folder for easier access.

4. Crop ROIs
Extract ROIs using annotations and display a sample.

5. Enhance Contrast
Apply CLAHE (local histogram equalization) to enhance image contrast.

6. Noise Reduction
Apply a Median filter to the equalized ROI images to remove noise.

7. Manual Thresholding with Seeded Region Growing
Apply seeded region growing on preprocessed images to determine thresholds manually by experimenting with various values, as the dataset lacks specific thresholds per image (as advised by the professor).

8. Extracting Intensity Features

Mean
Variance
Entropy
Energy
Skewness
Kurtosis
Contrast
9. Dataset Preprocessing
Preprocess the dataset and add the manually estimated thresholds for each image.

10. Threshold Prediction with ANN
Use an Artificial Neural Network to predict thresholds based on intensity features.

11. Dataset with Predicted Thresholds
Create a new dataset incorporating thresholds predicted by the ANN for each image.

12. Seeded Region Growing (Segmented and Ground Truth Images)
Apply seeded region growing using both predicted and manually calculated thresholds to generate segmented and ground truth images.

13. Update Data Frame
Add paths for segmented and ground truth images to the data frame.

14. Image Comparison
Compare original images, segmented images, and ground truth images side by side for evaluation.

15. Performance Metrics
Calculate DICE and Jaccard metrics to evaluate the similarity between segmented images and ground truth images.
