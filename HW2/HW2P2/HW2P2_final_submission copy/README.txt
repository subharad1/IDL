- **Model**: Model archtiecture description. Anything unique? Any specific architecture shapes or strategies?
- **Training Strategy**: optimizer + scheduler + loss function + any other unique ideas
- **Augmentations**: augmentations if used. If augmentations weren't used, then ignore
- **Notebook Execution**: Any instructions required to run your notebook.
I used a ResNet model for training the model. The model is not exactly but almost a ResNet34, altered to make sure the parameters do not cross 30M. 
I used the ArcFace with cross entropy loss, along with the weighted loss functions with ArcFace and ConstrativeLoss with the loss function switching fully to Constrastive at epoch 20.
Along with that, I used the SGD optimizer with learning rate of 0.01, and a CosineAnnealingLR for the scheduler, the scheduler also used a warmup with linearLR the first 5 epochs.
For the augmentations, I used RandomResizedCrop, RandomHoerizontalFlip, RandomRotation, RandomGrayscale, RandomErasing, and ColorJitter.
The notebook was executed as is on kaggle.