# IAM Line Segmentation Using Seam Carving

This algorithm segments handwritten text lines from the IAM dataset using seam carving.

### Pipeline

1. **Region of Interest Extraction (Image 1):** Crops the region between horizontal divider lines.
2. **Otsu Binarization (Image 2):** Converts the grayscale image into a binary image.
3. **Gaussian Filtering (Image 3):** Applies Gaussian blur to prepare the image for further processing.
4. **Horizontal Projection Profile (Image 4):** Computes and smooths the HPP to detect peaks and define line blocks.
5. **Energy Map Generation (Image 5):** Computes an energy map from the Gaussian-filtered image.
6. **Seam Carving (Image 6):** Finds low-energy horizontal seams within each block to segment the handwritten lines.
