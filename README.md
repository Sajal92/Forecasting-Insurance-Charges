# Deploy Machine Learning Pipeline on Google Kubernetes Engine
# Coding Challenge - Martian Robots

## Instructions to Run

* Open terminal inside the folder containing the source code i.e app folder
* To run the unit tests just type the command ``` pytest ``` and press enter
* To get the flask api up and running use following commands
```
docker image build -t rover .
docker run -p 5000:5000 -d rover

```

* Go to your browser and type the url: <localhost:5000>
* There you can enter inputs for rove

## Brief Introduction
Code has been developed using TDD approach in a OOP layout and supplied as a python package. 
A brief explanation of the code:
* navigate.py contains the MarsRover class which provides the functionalities to navigate the rover on plateau
* app.py conatins the flask api wrapper for the MarsRover class
* test_navigate.py contains various unit-tests eg. hard coded test cases, tests for missing entries, rover lost and clash test cases, invalid entries cases etc.
* API runs in a docker container with configuration provided in Docerfile
  
#### Assumptions:
* Rovers are landed and navigated on the plateau sequentially
* The lower-left coordinates of plateau are assumed to be 0,0.
* No limit for the number of rovers


## What Needs Improvement
* Get jsdom to work correctly in jest to write tests against App and Board
* Use react.js or vue.js or some other front end library to remove the DOM dependancy in some classes
* Make the UI pretty
* Parse the input in a way that the user can see the robots move around the screen



#### Sample Input
```
5 3
1 1 E
RFRFRFRF

3 2 N
FRRFLLFFRRFLL

0 3 W
LLFFFLFLFL
```
#### Sample Output
```
1 1 E
3 3 N LOST
2 3 S
```

