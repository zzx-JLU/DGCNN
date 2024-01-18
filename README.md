# DGCNN

This is a rough reproduction of the paper [EEG Emotion Recognition Using Dynamical Graph Convolutional Neural Networks](https://ieeexplore.ieee.org/document/8320798/), including the dynamical graph convolutional layer only. The code is adapted from [this open access repository](https://github.com/lehaifeng/T-GCN/blob/master/T-GCN/T-GCN-PyTorch/README.md).

To run the code, you can use commands below:

```
# GCN
python main.py --model_name GCN --max_epochs 3000 --learning_rate 0.001 --weight_decay 0 --batch_size 64 --hidden_dim 100 --settings supervised --gpus 1

# DGCNN
python main.py --model_name DGCNN --max_epochs 3000 --learning_rate 0.001 --weight_decay 0 --batch_size 64 --hidden_dim 100 --settings supervised --gpus 1
```

The value of parameters like `max_epochs`, `learning_rate` can be adjusted.

Run `tensorboard --logdir lightning_logs/version_0` to monitor the training progress and view the prediction results.
