Running Policy Gradient BROIL:
==================================
To run BROIL VPG:
In the spinningup/spinup/algos/pytorch/vpg directory run
```bash
python broil_vpg2.py --env (CartPole-v0, PointBot-v0)
```
Pass in BROIL arguments using
```bash
--broil_lambda
--broil_alpha
```
(Can also pass in all of the arguments listed in the original spinningup vpg.py code, ie: seed, epochs, env_name, policy_lr, etc)


==================================
To run BROIL PPO:
In the spinningup/spinup/algos/pytorch/ppo directory:

First create a folder (broil_dataX) and 3 subfolders (results, visualizations, PointBot_networks) within the PPO directory. Make sure to rename "broil_dataX" on line 476 so files are saved in the right folder. Then run the following command for a grid_search:

python3 broil_ppo.py --env PointBot-v0 --grid_search True


Default Arguments are defined in lines 507-522
File saving file directories are defined in lines 466-501
Alpha, Lambda, pi_lr, and vf_lr parameter arrays are defined in lines 539-546 to run multiple parameters
I also changed train_pi_iters from 80 to 40 on line 111.



Welcome to Spinning Up in Deep RL!
==================================

This is an educational resource produced by OpenAI that makes it easier to learn about deep reinforcement learning (deep RL).

For the unfamiliar: [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning) (RL) is a machine learning approach for teaching agents how to solve tasks by trial and error. Deep RL refers to the combination of RL with [deep learning](http://ufldl.stanford.edu/tutorial/).

This module contains a variety of helpful resources, including:

- a short [introduction](https://spinningup.openai.com/en/latest/spinningup/rl_intro.html) to RL terminology, kinds of algorithms, and basic theory,
- an [essay](https://spinningup.openai.com/en/latest/spinningup/spinningup.html) about how to grow into an RL research role,
- a [curated list](https://spinningup.openai.com/en/latest/spinningup/keypapers.html) of important papers organized by topic,
- a well-documented [code repo](https://github.com/openai/spinningup) of short, standalone implementations of key algorithms,
- and a few [exercises](https://spinningup.openai.com/en/latest/spinningup/exercises.html) to serve as warm-ups.

Get started at [spinningup.openai.com](https://spinningup.openai.com)!


Citing Spinning Up
------------------

If you reference or use Spinning Up in your research, please cite:

```
@article{SpinningUp2018,
    author = {Achiam, Joshua},
    title = {{Spinning Up in Deep Reinforcement Learning}},
    year = {2018}
}
```
