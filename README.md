# CompoundE3D

Code for "Knowledge Graph Embedding with 3D Compound Geometric Transformations"

## OGB installation

https://github.com/snap-stanford/ogb

#### Recommended order of installation 
 - Create a python 3.8.8 environment using Anaconda
 - Install torch 1.11.0 using Anaconda
 - Install torch-geometric using Anaconda
 - Install ogb using pip
 - Install other packages using pip

## After installing the OGB environment, to reproduce the results

```
CUDA_VISIBLE_DEVICES=0 python run.py --do_train --cuda --do_valid --do_test --evaluate_train \
            --model CompoundE -n 125 -b 8192 -d 300 -g 8 -a 1.0 -adv -tr \
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