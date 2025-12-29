\# Diffusion Disk Analyzer for SEM Images



Diffusion Disk Analyzer is a MATLAB App Designer application for quantitative

analysis of nanoholes and their associated diffusion disks from SEM images.



The app allows interactive selection of nanoholes in SEM images, automatic

segmentation using k-means clustering, ellipse fitting, and extraction of

nanohole diameters and diffusion disk radii along horizontal and vertical

directions. Results are exported automatically as images and Excel files.



---



\## Features



\- Load SEM images from `.tiff` (or other supported image formats)

\- Automatic detection of pixel size from image metadata (if available)

\- Manual input of pixel size (nm) if metadata is missing

\- Interactive rectangle selection around nanoholes

\- Automatic segmentation of:

&nbsp; - nanohole

&nbsp; - diffusion disk

\- Ellipse fitting to nanohole and diffusion disk regions

\- Extraction of:

&nbsp; - nanohole major and minor diameters

&nbsp; - diffusion disk radii (horizontal and vertical)

\- Automatic numbering of nanoholes

\- Export results to Excel and PNG



---



\## Input format



\- SEM image file (e.g. `.tiff`)

\- Image may be grayscale or RGB

\- Pixel size is:

&nbsp; - read automatically from metadata if available, or

&nbsp; - requested from the user in nanometers



---



\## How to run



1\. Open MATLAB

2\. Make sure `diffusion\_disk\_analyzer.mlapp` is on the MATLAB path

3\. Launch the app:

&nbsp;  ```matlab

&nbsp;  diffusion\_disk\_analyzer

&nbsp;  ```



---



\## Workflow



1\. Click \*\*Enter SEM file\*\* and load the SEM image

2\. If pixel size metadata is unavailable:

&nbsp;  - Enter pixel size manually (nm per pixel)

3\. Draw rectangles around each nanohole:

&nbsp;  - Include the nanohole

&nbsp;  - Include the full diffusion disk

&nbsp;  - Include some background

4\. After each rectangle:

&nbsp;  - Nanohole and diffusion disk are segmented automatically

&nbsp;  - Ellipses are fitted and displayed

5\. Repeat for all nanoholes

6\. Click \*\*Done\*\* to export results



---



\## Output



\### Image file (`\*\_fitted\_ellipses.png`)



\- Original SEM image

\- Fitted ellipses:

&nbsp; - Green: nanoholes

&nbsp; - Red: diffusion disks

\- Nanoholes are automatically numbered



\### Excel file (`\*\_analysis.xlsx`)



For each nanohole:

\- Nanohole major axis length \[nm]

\- Nanohole minor axis length \[nm]

\- Diffusion disk radius (major direction) \[nm]

\- Diffusion disk radius (minor direction) \[nm]



The last row contains:

\- Mean ± standard deviation for all measurements



---



\## MATLAB requirements



\- MATLAB R2021a or newer (recommended)

\- App Designer

\- Image Processing Toolbox

\- Statistics and Machine Learning Toolbox



---



\## Notes



\- Designed for manual, expert-guided SEM analysis

\- Robust to asymmetric nanoholes and diffusion disks

\- Segmentation is based on k-means clustering

\- Ellipse fitting is performed using region properties



---



\## Author



Your Name  

Affiliation (optional)



