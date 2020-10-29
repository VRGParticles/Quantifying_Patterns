# Quantifying_Particles
Repository for quantifying patterns in optical micrographs of one- and two-dimensional ellipsoidal particle assemblies.

The corresponding manuscript, *Quantifying patterns in optical micrographs of one- and two-dimensional ellipsoidal particle assemblies*, can be found [here](https://pubs.rsc.org/en/content/articlelanding/2020/sm/d0sm01692f#!divAbstract).

This repository provides image analysis for micrographs of polymorphic particle/colloid assemblies.  
Ellipsoidal particles are classified into chain lengths and symmetry groups.  

# What is Included #
There are three folders, one for each algorithm / particle classifier.


**MATLAB Files (.m):**

*Chain_Counter_1D:* Classify particles into chains and count the amount of chains.

*cmm_vs_p4m:* *p4m* plane symmetry group, *cmm* plane symmetry group,  Boundary, and Disorder (none of the 3 previous classes).

*cmm_vs_pgg:* *pgg* plane symmetry group, *cmm* plane symmetry group,  Boundary, and Disorder (none of the 3 previous classes).


Associated **parameter files** are included to replicate the results found in the manuscript (.csv).


### General Algorithm Overview
These algorithms classify particles based on classification conditions determined from interparticle distance and difference in particle orientation relationships. 
These two parameters are used to create further conditions, such as an amount of neighbors meeting a certain angle criteria or class criteria, to further classify particles.
Each part of the script is sectioned and commented to specify what conditions are being used to classify the particles.  For each classification algorithm,
the conditions are customized to the desired output, for example, amount of neighboring particles to meet classification conditions.

## Getting Started
*MATLAB Requirements*

To use these files, you must have MATLAB installed.  Scripts were written using MATLAB R2019b. These algorithms use the Image Processing Toolbox and the Statistics and Machine Learning Toolbox.

*Input Files*
The raw images/micrographs are located as Supplementart Images (availability pending publication).


## Running the Scripts

All input variables are toggleable using the interface controls in the LiveScript.
To run the script, the path/directory of the image must be navigated to, and the correct file name input into the 'file_name' box.
All other parameters below this variable are pre-loaded with one of the parameters found in the script folder repository.  For a new image, these parameters will have to be tweaked until appropriate for the image. The user should go chronologically down the script to modify each parameter.
```
Tip: For analysis of your own image (not provided by this repository),
the user should use the interface controls to tweak and perfect the
input parameters for the image, step-by-step. Once these parameters 
are determined, the figure creation of these sections can be surpressed 
by removing the check from the associated boxes. This will save time when 
analyzing the figure.
```
When the script is then run, the image(s) are read into the workspace and analyzed. 
```
Tip: To determine the distance threshold, D, the user can use a cropped
region of the image for the first run to get the range for D. Then, the
' Determine appropriate distance threshold (D)' section can be surpressed 
for future runs of the same image. Else, the user can zoom into one section
of the image to find the appropriate particle numbers.
```

### Analysis Outputs
These algorithms can create labeled images, bar charts quantifying the particle classification, and associated Excel files. The outputs are dependent on the boxes the users check off. Figures of the intermediate steps can also be created if their associated boxes are ticked, but are typically not needed beyond input parameters being determined.
For record-keeping, an Excel file of each of the input parameters is also output per image.


### More Advanced Script Customization 

Each of these algorithms were created specifically to the input files noted in the *Getting Started* section above.  For more advanced image analysis, 
i.e. customizing these algorithms more toward a user-provided image instead of the provided input files, the user can edit the script, 
and ultimately what the final classification criteria is for each class.  The user can edit typical classification criteria at any step using the interface controls in the LiveScript. More advanced users can modify the sections to their own needs, especially in the 'Modify Requirements' section, which is typically custom per image.

```
Tips: Once the desired parameters are found/testing parameters for the image is no longer needed, the 
figure creation within MATLAB can be suppressed by unchecking boxes in sections no longer needed.
The scripts can be saved as '.m' files to speed up run times.
```


### Troubleshooting
*If a user-provided image is used instead of the provided input files*
```
Tip: To go step-by-step during segmentation, the line 'return'
can be added to stop the script from running at that line. 
```
Each line can also be edited, if need be, to fit the image.
MATLAB related issues can be solved by viewing the [MATLAB documentation.](https://www.mathworks.com/help/index.html)

### Author

* **Veronica Grebe** - [Weck Group, New York University](http://weckresearch.com/home)

For a full list of manuscript authors who contributed to the overall project, see the [manuscript](https://pubs.rsc.org/en/content/articlelanding/2020/sm/d0sm01692f#!divAbstract).

### License

This project is licensed under the GNU GPL-3.0 License - see the [LICENSE](LICENSE) file for details

### What is Next?
Stay tuned for more particle image analysis!

