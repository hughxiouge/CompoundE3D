# CompoundE3D

Code for "Knowledge Graph Embedding with 3D Compound Geometric Transformations"

## OGB installation

https://github.com/snap-stanford/ogb

#### Environment setup guide
 - Create a python environment using Anaconda
 - Install latest version of torch using Anaconda
 - Install latest version of torch-geometric using Anaconda
 - Install ogb using pip
 - Install tensorboardx using pip

## After installing the OGB environment, to reproduce the results

```
CUDA_VISIBLE_DEVICES=0 python run.py --do_train --cuda --do_valid --do_test --evaluate_train \
            --model CompoundE3D_Complete_Mix_T_H -n 125 -b 8192 -d 300 -g 8 -a 1.0 -adv -tr \
            -lr 0.001 --max_steps 300000 --cpu_num 8 --test_batch_size 32  --print_on_screen
```

**Citation**

If you find the source codes useful, please consider citing our [paper](https://arxiv.org/abs/2304.00378):

```
@article{ge2023knowledge,
  title={Knowledge Graph Embedding with 3D Compound Geometric Transformations},
  author={Ge, Xiou and Wang, Yun-Cheng and Wang, Bin and Kuo, C-C Jay},
  journal={arXiv preprint arXiv:2304.00378},
  year={2023}
}
```