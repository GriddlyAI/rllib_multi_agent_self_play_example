# RLlib Multi Agent Self-Play Example - MultiPlayer Gridman

In this version of the GridMan environment you train gridman but also his enemies!

GridMan and the 3 enemies all have completely seperate neural networks and separate rewards.

<div style="text-align: center">
    <img src="./assets/level_0.gif" width="250" />
    <img src="./assets/level_1.gif" width="250" />
    <img src="./assets/level_2.gif" width="250" />
</div>

More documentation can be found [here](https://griddly.readthedocs.io/en/latest/rllib/multi-agent/index.html)

This repository can be used as a starter for training any of the Griddly environemnts using RLLib

## Installing Dependencies

We use poetry to manage the dependencies of this project. You can set up a poetry environment with the command:

```commandline
poetry install
```

You can then activate the poetry environment using:

```commandline
poetry shell
```

## Training the example environment

```commandline
python train.py
```

### Options for training

There are three variables that you can change in train.py:

```python
environment_name = "TestEnvironment"
environment_yaml = "gridman/gridman_multiagent.yaml"
gridman_model_name = "SimpleConvAgent"
enemy_model_name = "SimpleConvAgent"
```

#### environment_name

The name of the environment

#### environment_yaml

the yaml file containing the GDY of the environment

#### model_name

We provide two simple models that can be used are `SimpleConvAgent` and `GlobalAveragePoolingAgent`

## Weights and Biases

You can find training information here:

https://wandb.ai/griddlyai/RLLib%20Gridman%20MultiAgent

## Citing

If you use this environment, please cite the original Griddly Paper: 

```commandline
@article{
  author    = {Chris Bamford and
               Shengyi Huang and
               Simon M. Lucas},
  title     = {Griddly: {A} platform for {AI} research in games},
  journal   = {CoRR},
  volume    = {abs/2011.06363},
  year      = {2020},
  url       = {https://arxiv.org/abs/2011.06363},
  eprinttype = {arXiv},
  eprint    = {2011.06363},
}
```
