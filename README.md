# Classical Planning #

You can find here a classical planning the farmbot executes completely coded using the python language.

### Files explanation ###

- **newfileplanning.py** generates the domain.pddl file and the problem.pddl file (easier way to write pddl files using python language) with cmd: ***python -m py2pddl.parse newfileplanning.py***
- **execute.txt** is the classical planning generated by the ff solver using the domain.pddl file and the problem.pddl file with cmd: ***./ff -o domain.pddl -f problem.pddl >execute.txt***
- **torobot.py** file contains the file that should be sent to the robot so it executes everything
- **plan02.py** (parser) reads execute.txt and generates commands.txt
- **commands.txt** contains the saved vector containing all the cmds that will be executed by the robot using the torobot.py file
- **data.csv** the values of the soil sensor are stored in this file in the form of a csv file
- The file ff-v2.3.zip file should be extracted to obtain the ff solver. It has been downloaded from: https://fai.cs.uni-saarland.de/hoffmann/ff.html 

### How to run the code ###

In short the user should 
1. run the new.file.planning.py to create the 2 pddls files
2. run the ff solver to generate the classical planning and put the result in execute.txt
3. run the plan02.py file to parse the classical planning which will sqve the result in commands.txt
4. run the torobot.py file which will run the robot.

### Requirements ###

- Farmbot library
- csv library
- py2pddl library


:four_leaf_clover: # IMAGE PROCESSING #

You can find here the methodology used to analyze the photos taken from the Farmbot.

### The code ###

To do this we used an already done plant segmentation github repository: https://github.com/otaviog/plant-segmentation

PS:
- The reauirements for python 3.7 should be respected the Ubuntu one is not necessary.
- The command that should be written in the terminal at the later stages of using this repository shouold be:
"rflow fpn run train" and not "rflow run fpn train".

### The Dataset ###

The Dataset used is through a link shown in the plant segmentation github repository  mentioned above: https://github.com/otaviog/plant-segmentation

# Markov Decision Process #

MDP_plan_02.ipynb file defines the problem with the Markov Decision Process.
