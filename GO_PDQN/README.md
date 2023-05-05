# GO_PrioritizedDQN

Vanilla PDQN with Go_Explore

The notebook is designed to work with Paperspace Gradient since Google Colab's update to 3.9 has broken older versions of OPen AI gym.

If you would like to use Kaggle instead then after install gym==0.19 add the following cell:

```python
!apt-get install unrar
```

Algorithm results below:



PDQN:

![PDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DoubleDQN/DoubleDQN_Vanilla.png "PDQN_Vanilla")

GO_PDQN:

![GO_PDQN](https://github.com/robjlyons/GO_DQN/blob/main/GO_DoubleDQN/GO_DoubleDQN.png "GO_PDQN")

Note: I have added annealing to the learning rate for the GO_DoubleDQN version, the output spits out a warning about it but there is a noticable increase in performance.
