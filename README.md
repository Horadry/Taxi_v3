# Taxi_v3
My solution to the OpenAI Taxi-v3 task

https://www.gymlibrary.ml/environments/toy_text/taxi/?highlight=taxi

## Description: 

There are four designated locations in the grid world indicated by R(ed), G(reen), Y(ellow), and B(lue). When the episode starts, the taxi starts off at a random square and the passenger is at a random location. The taxi drives to the passenger’s location, picks up the passenger, drives to the passenger’s destination (another one of the four specified locations), and then drops off the passenger. Once the passenger is dropped off, the episode ends.

#### Actions:

    There are 6 actions:
    0: move south / 1: move north / 2: move east / 3: move west / 4: pickup passenger / 5: drop off passenger

#### States:   

    We have 500 discrete states, each state space is represented by the tuple: (taxi_row, taxi_col, passenger_location, destination)   

#### Rewards:   

    -1 per step unless other reward is triggered.

    +20 delivering passenger.

    -10 executing “pickup” and “drop-off” actions illegally.


    
## Methods:

### 1. Q-learning

#### My hyperparameters:

    Number of episodes: 50000 

    Max steps per episode: 99 

    Learning rate: 0.06

    Discount rate (gamma): 0.86

    Exploration rate: epsilon = 0.95, epsilon_min = 0.01   

    Decay rate: 0.0099   



## Results:

    | Method        | Score         |
    | ------------- | ------------- |
    | Q-learning    | 8.24          |
    |               |               |
