# MTM-identifying-trees

## About the project:

## Steps:

1. Download Anaconda https://www.anaconda.com/products/individual
2. In the Anacona Prompt, enter the following commands:

    Create a python environment
    ```
    conda create -n pyEnv python=3.9
    conda activate pyEnv
    ```
    
    Install libraries
    ```
    conda install -c conda-forge opencv
    conda install -c conda-forge matplotlib
    conda install -c conda-forge spyder
    ```
    
    Launch Spyder:
    ```
    spyder
    ```
3. Download or clone this repository to run the source code on spyder.

## Input Image Requirements:

1. Use PNG for more accurate results.
2. Image must be of a 64 hectare (800m by 800m) plot of land.
3. Hue will need to be adjusted according to the image (Example images and hues can be found in the test_image directory).

## How to Run the code:

In  `TreeDetectionAlgorithm.py`
* update `img = cv2.imread("image.PNG")` with the image filename/filepath. (For example `img = cv2.imread("test-images\OnePlot.PNG")`)
* adjust `lower_color = np.array([40, 20, 0])` with the corresponding Hue (the first number)

Run the program.

## Output:

The program outputs:
* an image with tree areas surrounded by either green or red
* the final area

The areas in green are less than 1 hectare and are included in the final area.

The areas in red are larger than 1 hectare, which are not included in the final area.

<img src="https://github.com/thanujasiva/MTM-identifying-trees/blob/main/test-images/IsolatedHouse.png" align="left" height="48" width="48" >


### Example Output:
```
Size of image in pixels: 1062 x 1039
Area of trees in pixels: 53451.5
Area of trees in hectares: 3.100272063714748
Percentage of area covered by trees: 4.84 %
```

## Contributors:

* Shrimei Chock
* Maisha Abdullah
* Thanuja Sivaananthan

## Sources:
