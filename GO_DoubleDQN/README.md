# GO_DQN

Vanilla DDQN with Go_Explore

The below graphs are both trained with the same hyperparamaters for 1e6 frames on Pong. The only change being to run Go_Explore on or off.

The notebook is designed to work with Paperspace Gradient since Google Colab's update to 3.9 has broken older versions of OPen AI gym.

If you would like to use Kaggle instead then after install gym==0.19 add the following cell:

```python
!apt-get install unrar
```

Algorithm results below:

Similarly to the DQN results, Vanilla is better performing but this is likely due to the GO-Explore version going back to explore more states. The GO_DoubleDQN performs much better than the regular GO_DQN.

DoubleDQN:

![DoubleDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DoubleDQN/DoubleDQN_Vanilla.png "DoubleDQN_Vanilla")

GO_DoubleDQN:

![GO_DoubleDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DoubleDQN/GO_DoubleDQN.png "GO_DoubleDQN")

GO_DoubleDQN_NonEpisodic:

To Be Added

This version makes a few changes:

1. Instead of saving/loading the state for the 'return' fuction of go explore we walk through the trajectory.
2. Instead of reseting the game we save cellhashes and then check if there is a trajectory between the current frame and the ram cellhash and 'return' that way. If no cellhash/ram combination can be found then reset and walk through the trajectory back to ram.
