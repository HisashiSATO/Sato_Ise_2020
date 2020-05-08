______________________________________________________
Sato and Ise (submitted) Open Data

Author: Hisashi SATO (JAMSTEC) hsatoscb_(at)_gmail.com

Date: 8 May 2020

URLs:

https://github.com/HisashiSATO/Sato_Ise_2020

https://ebcrpa.jamstec.go.jp/~hsato/Sato_and_Ise_2020

Notice:
Visualized Climate Environments (VCEs) are only available at the latter URL due to the limitation of file size.
______________________________________________________

1. Folder "1.VCDs"
It contains Visualized Climate Environments (VCEs) for training and testing the Convolutional-Neural-Network (CNN) model. Names of compressed files (*.tar.gz) correspond to experiments. Each compressed file contains 4 to 16 folders.

Naming rule of folders:
The strings "CRU", "NCEP", "HadGEM", and "Miroc" stand for that the files are made from CRU_TS4.0, NCEP/NCAR reanalysis, Had2GEM-ESM, and Miroc-ESM climate datasets, respectively. The strings "AMeans" and "MMeans", respectively, stand for that annual-mean and monthly-mean climates are represented by VCEs in the compressed file.
The string "EachYear" means that the compressed files contains VCEs of each year climate from 1971 to 1980, otherwise the compressed files contains VCEs of averaged climate over 10 years. The strings "hist", "RCP26", and "RCP85" mean that the compressed files contain VCEs of climate averaged over 1971-1980, 2091-2100@RCP2.6, and 2091-2100@RCP8.5, respectively.

MainSimulation_training.tar.gz
VCEs for training the CNN model for the main simulation and dependency test of climatic datasets for training and reconstructing performances.

MainSimulation.tar.gz
VCEs for testing the CNN model for the main simulation.

CombinationSelection_Amean.tar.gz
VCEs for an experiment to find optimal combination of climatic variables (annual means) represented by the VCEs. In the VCE of the RGB color tile, up to three climate variables can be represented by RGB channels. To find the optimal combination of climatic variables, we systematically evaluated the model performance of 14 combinations of climatic variable experiments for annual means. It's result is presented in the Supplemental Material 2.
Extracting this compressed fire results in "CRU", "NCEP", "HadGEM", and "Miroc" folders. Each folder contains 14 subfolders named with sequential numbers, which corresponds to model numbers in the Supplemental Material 2.

CombinationSelection_Mmean.tar.gz
Same as the CombinationSelection_Amean.tar.gz except made with monthly mean climates, and related information is available in the Supplemental Material 3.

ScalerSelection.tar.gz
VCEs for evaluate the influences of different transformations of climatic variables on the resulting accuracy. It's result is presented in the Supplemental Material 4.
Extracting this compressed fire results in "CRU", "NCEP", "HadGEM", and "Miroc" folders. Each folder contains 4 subfolders named with sequential numbers. "Scaler1" stands for log transformed, "Scaler2" stands for no transformed (linear), "Scaler3" stands for Sigmoid(gain=5) transformed, "Scaler4" stands for Sigmoid(gain=10) transformed.

ColorAssignExperiment.tar.gz
VCEs for evaluate the influences of assignment patterns of air temperature and precipitation to RGB color channels of the VCE. It's result is presented in the Supplemental Material 5. Extracting this compressed fire results in "CRU", "NCEP", "HadGEM", and "Miroc" folders. Each folder contains 6 subfolders named with sequential numbers, which indicates model number in the Supplemental Material 5.


Individual VCE shows climatic condition of each half degree grid cell. According to the ISLSCP2 data, VCEs are classified by their their potential vegetation type of the grid. Number of deepest folder names correspond vegetation code of the ISLSCP2.

Following are the vegetation code.
   01: Tropical Evergreen Forest/Woodland
   02: Tropical Deciduous Forest/Woodland
   03: Temperate Broadleaf Evergreen Forest/ Woodland
   04: Temperate Needleleaf Evergreen Forest/Woodland
   05: Temperate Deciduous Forest/Woodland
   06: Boreal Evergreen Forest/Woodland
   07: Boreal Deciduous Forest/Woodland
   08: Evergreen/Deciduous Mixed Forest
   09: Savanna
   10: Grassland/Steppe
   11: Dense Shrubland
   12: Open Shrubland
   13: Tundra
   14: Desert
   15: Polar Desert/Rock/Ice

Naming rule for VCEs of 10 years average climate is following:
Latitude number + "_" + Longitude number + ".png"

Naming rule for VCEs of each year climate is following:
Latitude number + "_" + Longitude number + "_" + Year of climate + ".png"

Here, latitude number ranges from 001 to 360, starting from north-latitude-90 to southward with half degree interval. The longitude number ranges from 001 to 720, starting from west-longitude-180 to eastward with half degree interval. 

On the top of this subfolder, there is PicList.zip, which is a compressed file of PicList.txt. This text file is 
required for classify VCEs with the trained model.

_____________________________________________
2. Folder "2.Result"
It contains copies of image classifications results of the Digits screen. 
Subfolder names correspond to experiment names. Each subfolder contains subsub-folders "DigitsOutput", "ConfusionMatrix", and "ReconstructedBiomeMap". Naming rules for files are basically same as those of VCEs.

_____________________________________________
3. Folder "3.LearningCurves"
It contains screen capture of Digits output, showing learning curve of CNN models. CRU climate data. This folder contains 5 subfolders. Naming rules of these subfolders are same as those of VCEs.

_____________________________________________
4. Folder "5.FigureMaterials" 
It contains data and codes (in R) for drawing the figures in the manuscript"

_____________________________________________________________
