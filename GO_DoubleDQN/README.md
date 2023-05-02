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

Note: I have added annealing to the learning rate for the GO_DoubleDQN version, the output spits out a warning about it but there is a noticable increase in performance.
