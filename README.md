# OptimizedLR

OptimizedLR is a Python package for finding the best learning rate for your model.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install OptimizedLR.

```bash
pip3 install OptimizedLR
```
## Requirements
You also need to install TensorFlow, I didn't include them due to problems the Mac M1 user will face.
## Usage

```python
from optimal_LR import OptimizedLR

# initialize the object, we need the model created and compiled and the learning rate min value
lrs_finder = OptimizedLR(model, 3e-6)

# we search for the best lr, we need the validation_data to be passed
lrs_finder.search(train_data,train_targets, validation=(test_data, test_targets), epochs= 10, batch=16)
# we plot an interactive visualization of the validation loss and the learning rates
lrs_finder.plot_loss()
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
Plotly won't load the plot in colab.
Please make sure to update tests as appropriate.

## License
University Moulay Sultan Slimane.
