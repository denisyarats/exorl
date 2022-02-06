

# ExORL: Exploratory Data for Offline Reinforcement Learning

This is an original PyTorch implementation of the ExORL framework from

[Don't Change the Algorithm, Change the Data: Exploratory Data for Offline Reinforcement Learning](https://arxiv.org/abs/2201.13425) by

[Denis Yarats*](https://cs.nyu.edu/~dy1042/), [David Brandfonbrener*](https://davidbrandfonbrener.github.io/), [Hao Liu](https://www.haoliu.site/), [Misha Laskin](https://www.mishalaskin.com/), [Pieter Abbeel](https://people.eecs.berkeley.edu/~pabbeel/), [Alessandro Lazaric](http://chercheurs.lille.inria.fr/~lazaric/Webpage/Home/Home.html), and [Lerrel Pinto](https://www.lerrelpinto.com).

*Equal contribution.

## Method


## Citation

If you use this repo in your research, please consider citing the paper as follows:
```
@article{yarats2022exorl,
  title={Don't Change the Algorithm, Change the Data: Exploratory Data for Offline Reinforcement Learning},
  author={Denis Yarats, David Brandfonbrener, Hao Liu, Michael Laskin, Pieter Abbeel, Alessandro Lazaric, Lerrel Pinto},
  journal={arXiv preprint arXiv:2201.13425},
  year={2022}
}
```

## Instructions

Install dependencies:
```sh
conda env create -f conda_env.yml
conda activate exorl
```

Train the agent:
```sh
python train.py task=quadruped_walk
```

Monitor results:
```sh
tensorboard --logdir exp_local
```

## License
The majority of ExORL is licensed under the MIT license, however portions of the project are available under separate license terms: DeepMind is licensed under the Apache 2.0 license.
