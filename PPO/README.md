# pytorch-a2c-ppo-acktr
Code: https://github.com/ikostrikov/pytorch-a2c-ppo-acktr-gail

We use A2C-GRU, PPO-GRU in this repo as compared method in "standard" POMDPs.

## Installation
Please refer to `setup.py`

## Commands
We use the hyperparamters used in the original repository. 

```bash
export PYTHONPATH=${PWD}:$PYTHONPATH
python PPO/main.py --config configs/pomdp/ant_blt/p/ppo_rnn.yml \
     --algo ppo --lr 2.5e-4 --use-gae --entropy-coef 0.01 \
     --num-steps 128 --recurrent-policy
python PPO/main.py --config configs/rmdp/cheetah/ppo_rnn.yml \
    --algo ppo --lr 2.5e-4 --use-gae --entropy-coef 0.01 \
    --num-steps 128 --recurrent-policy
```
