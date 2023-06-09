# GO_DQN

Vanilla DQN with Go_Explore

The below graphs are both trained with the same hyperparamaters for 1e6 frames on Pong. The only change being to run Go_Explore on or off.

The notebook is designed to work with Paperspace Gradient since Google Colab's update to 3.9 has broken older versions of OPen AI gym.

If you would like to use Kaggle instead then after install gym==0.19 add the following cell:

```python
!apt-get install unrar
```

Algorithm results below:

The GO_Explore variant performs more consistently straight away but vanilla gets a much higher max score within the 1e6 steps.

DQN:

![DQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DQN/DQN_Vanilla.png "DQN_Vanilla")

GO_DQN:

![GO_DQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DQN/GO_DQN.png "GO_DQN")

GO_DQN_NonEpisodic:

![GO_DQN_NonEpisodic](https://github.com/robjlyons/GO_DQN/blob/main/GO_DQN/GO_DQN_NoResets.png "GO_DQN_NonEpisodic")

This version makes a few changes:

1. Instead of saving/loading the state for the 'return' fuction of go explore we walk through the trajectory.
2. Instead of reseting the game we save cellhashes and then check if there is a trajectory between the current frame and the ram cellhash and 'return' that way. If no cellhash/ram combination can be found then reset and walk through the trajectory back to ram.
3. Performance is so bad that I will not be continuing to try it.
