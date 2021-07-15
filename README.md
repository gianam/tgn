# TGN Demo

Prototype PopTorch implementation of [TGN](https://arxiv.org/abs/2006.10637).

This implementation is based on [`examples/tgn.py`](https://github.com/rusty1s/pytorch_geometric/blob/master/examples/tgn.py) from PyTorch-Geometric.

## Running on IPU

This repo needs the CPU version of `torch_geometric` (and its dependencies) to prepare the data. Make sure you don't install the CUDA version:

```bash
pip install -r tgn_requirements.txt
```

To run tests on a few modules:

```bash
python tgn_test.py
```

The notebook `side_by_side` runs this implementation against the reference implementation (note: a change is needed to pass all the tests, detailed in the notebook itself). This is included as a test and to understand step by step how the data and the memory are affected by vectorising the code and padding the variables to a static shape - it should provide a good way to follow naming conventions.




