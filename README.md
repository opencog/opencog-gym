# Rational OpenCog Controlled Agent
> Use OpenCog to control a rational agent in OpenAI Gym and Malmo environments.


OpenCog wrapper around OpenAI Gym.

Highly experimental at this stage.

## Requirements

OpenCog tools

- cogutil
- atomspace
- ure
- spacetime
- pln
- miner
- [optional] cogserver
- [optional] attention
- [optional] opencog

Third party tools

- Python 3
- python-orderedmultidict https://pypi.org/project/orderedmultidict/
- fastcore https://fastcore.fast.ai
- OpenAI Gym https://gym.openai.com/
- MineRL https://minerl.io
  - In the current release there is a trivial bug that prevents Minecraft from building, go to `.../site-packages/minerl/env/Malmo/Minecraft/build.gradle` and
    edit line 73 such that the URL uses HTTPS protocol (https://github.com/minerllabs/minerl/issues/450#issuecomment-777009360).
- nbdev https://nbdev.fast.ai

## Install

In the root folder enter the following command:

```bash
pip install -e .
```

## How to use

For now a gym agent defined under the `rocca/agents` folder is provided that
can used to implement agents for given environments.  See the examples
under the `examples` folder.


There are Jupyter notebooks provided for experimentation as well.

## Develop

You do not have to use `nbdev` to work with the code under the `rocca` directory.
You should use it though if you want to work with Jupyter notebooks, the repository is setup to use certain
utilities to clean them from unnecessary metadata when committing.


One important mention is that `README.md` is now generated from `index.ipynb` by `nbdev_build_docs` command.
Thus, you should not edit `README.md` directly.


Exports from notebooks are generated with `nbdev_build_lib`. Changes to the exported code can be synchronized
back to notebooks with `nbdev_update_lib`.
