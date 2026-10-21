# IAM Line Segmentation Using Seam Carving

This algorithm segments handwritten text lines from the IAM dataset using seam carving.

### Pipeline

1. **Region of Interest Extraction (Image 1):** Crops the region between horizontal divider lines.

![Region of Interest](images/01.png)

2. **Otsu Binarization (Image 2):** Converts the grayscale image into a binary image.

![Otsu](images/02.png)
   
3. **Gaussian Filtering (Image 3):** Applies Gaussian blur to prepare the image for further processing.

![Gaussian Filter](images/03.png)
   
4. **Horizontal Projection Profile (Image 4):** Computes and smooths the HPP to detect peaks and define line blocks.

![HPP](images/04.png)
   
5. **Energy Map Generation (Image 5):** Computes an energy map from the Gaussian-filtered image.

![Energy Map](images/05.png)
    
6. **Seam Carving (Image 6):** Finds low-energy horizontal seams within each block to segment the handwritten lines.

![Seam Carving](images/06.png)
