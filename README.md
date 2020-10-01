# Introduction
A fine-tune of GaitSet and evaluate it on CASIA-B dataset.

# What we have done
We add a new module to extract the fine-grained feature.
And we also add a multi-layer feature fusion module to extract complementary information.

# Train or test
1. If you want to train the model on your dataset, you just need to configure the 'config.py' file to change the dataset path.
'''bash
python train.py
'''
2. If you just want to evaluate the model, you need to download the pretrained model and put it in "./work/checkpoint/GaitSet" folder.
'''bash
python test.py --iter=51700
'''
3. The pretrained model is avaliable: 'GaitSet_CASIA-B-51700-encoder.ptm' (link: https://pan.baidu.com/s/1Td_J-UPTqS8gmpBmq2_log code: hust)

# Comparsion
We evaluate our methods on CASIA-B dataset and compare it with GaitSet(AAAI 2018) and GaitPart(CVPR2020).
Because of our lab's server's problem, we can't evalute the method on the largest dataset named OU-MVLP.

## Table 1. Compasion with GaitSet on CASIA-B dataset.
---------------------------------------------------
model             |    NM    |    BG    |    CL    |
------------------|----------|----------|----------|
GaitSet           |   95.0%  |   87.2%  |   70.4%  |
Ours(Fine-tune)   |   96.8%  |   91.8%  |   78.0%  |
---------------------------------------------------

## Table 2. Comparsion with GaitPart on CASIA-B dataset.
---------------------------------------------------
model             |    NM    |    BG    |    CL    |
------------------|----------|----------|----------|
GaitPart          |   96.2%  |   91.5%  |   78.7%  |
Ours(Fine-tune)   |   96.8%  |   91.8%  |   78.0%  |
---------------------------------------------------

# Analyze the results
As we can see, We surpass GaitSet on three differnet sequences type.
We also surpass GaitPart on NM and BG, but our CL's accuracy is lower than GaitPart.

# Hope
Maybe there are tremendous tricks to boost the accuracy. Hope readers' commands!!!
