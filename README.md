

# ExORL: Exploratory Data for Offline Reinforcement Learning

This is an original PyTorch implementation of the ExORL framework from

[Don't Change the Algorithm, Change the Data: Exploratory Data for Offline Reinforcement Learning](https://arxiv.org/abs/2201.13425) by

[Denis Yarats*](https://cs.nyu.edu/~dy1042/), [David Brandfonbrener*](https://davidbrandfonbrener.github.io/), [Hao Liu](https://www.haoliu.site/), [Misha Laskin](https://www.mishalaskin.com/), [Pieter Abbeel](https://people.eecs.berkeley.edu/~pabbeel/), [Alessandro Lazaric](http://chercheurs.lille.inria.fr/~lazaric/Webpage/Home/Home.html), and [Lerrel Pinto](https://www.lerrelpinto.com).

*Equal contribution.

## Method



## Instructions

Install [MuJoCo](http://www.mujoco.org/) if it is not already the case:

* Obtain a license on the [MuJoCo website](https://www.roboti.us/license.html).
* Download MuJoCo binaries [here](https://www.roboti.us/index.html).
* Unzip the downloaded archive into `~/.mujoco/mujoco200` and place your license key file `mjkey.txt` at `~/.mujoco`.
* Use the env variables `MUJOCO_PY_MJKEY_PATH` and `MUJOCO_PY_MUJOCO_PATH` to specify the MuJoCo license key path and the MuJoCo directory path.
* Append the MuJoCo subdirectory bin path into the env variable `LD_LIBRARY_PATH`.

Install the following libraries:
```sh
sudo apt update
sudo apt install libosmesa6-dev libgl1-mesa-glx libglfw3 unzip
```

Install dependencies:
```sh
conda env create -f conda_env.yml
conda activate exorl
```

Download datasets by using `./download.sh <DOMAIN> <ALGO>` command, for example to download ProtoRL dataset for Walker, run
```sh
./download.sh walker proto
```
It will download the dataset from S3 and store it under `datasets/walker/proto/`, where you can find episodes (under `buffer`) and episode videos (under `video`).

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


## License
The majority of ExORL is licensed under the MIT license, however portions of the project are available under separate license terms: DeepMind is licensed under the Apache 2.0 license.
