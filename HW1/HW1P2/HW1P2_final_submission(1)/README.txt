The code run as is good to run for the best model performance. The model was a simple 5 layers model and the BatchNorm and Dropout in the first 2 layers and the input layer.
Used cross entropy loss function with label smoothing of 0.05, with a AdamW optimizer and learning rate of 0.001. The best performing scheduler is ReduceOnPleateau.
Both Time (9) and frequency (6) augmentation with 0.7 probability on the training dataset.
- **Model**: Model archtiecture description. Anything unique? Any specific architecture shapes or strategies?
- **Training Strategy**: optimizer + scheduler + loss function + any other unique ideas
- **Augmentations**: augmentations if used. If augmentations weren't used, then ignore
- **Notebook Execution**: Any instructions required to run your notebook.