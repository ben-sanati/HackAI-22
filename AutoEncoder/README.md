# Final Method

The final method was implemented in PyTorch, with the AutoEncoder trained in [autoEncoder.py](./autoEncoder.py) with the trained model being saved in [autoencode.pth](./autoencode.pth). This model can be loaded and used by doing the following:
```
    model = {Model_Class}().to(device)
    model.load_state_dict(torch.load(pthfile_location))
    model.eval()
```
It should be noted that the '''AutoEncoder''' class must be instanced in order to use the model as detailed above. 