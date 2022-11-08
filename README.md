This repo is meant as a collaborative digital platfrom to exchange files and tools among GIS labs to control ABB Robots in GIS facilities, in particular using COMPAS_RRC

# Setting up Compas RRC

## 1. Install [Anaconda](https://www.anaconda.com/products/distribution#Downloads)

## 2. & 3. Create a Conda environment, and Install COMPAS, COMPAS_FAB & COMPAS_RRC using Conda

+ in terminal [mac] / anaconda prompt [win]:
Creating the environment and installing COMPAS, COMPAS_FAB & COMPAS_RRC
```(base) conda config --add channels conda-forge
(base) conda create -n rrcgis -c conda-forge python=3.8 compas
(base) conda install -n rrcgis python=3.8 compas_fab
(base) conda install -n rrcgis python=3.8 compas_rrc
```
+ Activating the environment
`(base) conda activate rrcgis`
+ Verifying installation
`(rrcgis) python -m compas`


## 4. Add the Compas libraries to Rhino’s Python paths

+ in terminal `(rrcgis) python -m compas_rhino.install -v 7.0`

+ in Rhino (after restart if opened): 
`_EditPythonScript`, `import compas_fab` and run to verifying installation 

`_Grasshopper` Check the presence of a COMPAS FAB tab


## 5. Install Visual Studio Code + Docker and compose up the image file

+ Download & Install [Visual Studio Code](https://code.visualstudio.com/)
+ Download & Install [Docker Desktop](https://www.docker.com/products/docker-desktop)

*NOTE: After installation on Windows, it is normally required to enable Virtualization on the BIOS of the computer.*

+ Start Docker Desktop
+ In Visual Studio Code, right click on the appropriate docker compose image, and compose up

## 6. Open the Robot Playground grasshopper file

+ Open the file ABB_GoFa_robot_playground_RRCGIS_01.gh located in RRC-GIS/10_playgrounds/
+ Connect to ROS (Docker) and Load the robot
+ Explore forward kinematics, inverse kinematics, and pick & place

