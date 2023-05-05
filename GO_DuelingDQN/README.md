# GO_DuellingDQN

Vanilla DuellingDQN with Go_Explore

The notebook is designed to work with Paperspace Gradient since Google Colab's update to 3.9 has broken older versions of OPen AI gym.

If you would like to use Kaggle instead then after install gym==0.19 add the following cell:

```python
!apt-get install unrar
```

Algorithm results below:

Similarly to the DQN & DDQN results, Vanilla is better performing but this is likely due to the GO-Explore version going back to explore more states.

DuelingDQN:

![DuelingDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DuelingDQN/DuellingDQN_Vanilla.png "DuellingDQN_Vanilla")

GO_DuellingDQN:

![GO_DuellingDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DuelingDQN/GO_DuellingDQN.png "GO_DuellingDQN")

Note: I have added annealing to the learning rate for the GO_DuellingDQN version, the output spits out a warning about it but there is a noticable increase in performance.
