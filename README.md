# ml-kinect

## Frontend
There is the python frontend for ease of use, and then we have the c++ frontend for more extended functionality for specialized GPU kernels.
## Example

```python
from ml_kinect import Module, run
from torch import nn, Tensor
# Torch like declaration
class NeuralNetwork(Module):
    def __init__(self) -> None: #Predefined parameters or instantiated on inherited class
        super().__init__()
        self.net = nn.Sequential(
            nn.Linear(54, 10),
            nn.Linear(10, 1)
        )
        self.load_model_parameters(<model_path>)

    def forward(self, x: Tensor) -> Tensor:
        return self.net(x)

    def __loop__(self) -> None:
        #Define the inner loop
if __name__ == '__main__':
    run(Module) # Default run initialization
```
## Dependencies
```bash
sudo apt-get update
sudo apt-get install build-essential cmake pkg-config libusb-1.0-0-dev libudev-dev freeglut3-dev libxmu-dev libxi-dev libopenni2-dev libfreenect-dev libfreenect-bin libopencv-dev
```
## Citation

```
@misc{lightorch,
  author = {Jorge Enciso},
  title = {LighTorch: Automated Deep Learning framework for researchers},
  howpublished = {\url{https://github.com/Jorgedavyd/LighTorch}},
  year = {2024}
}
```
## Contact

- [Linkedin](https://www.linkedin.com/in/jorge-david-enciso-mart%C3%ADnez-149977265/)
- [GitHub](https://github.com/Jorgedavyd)
- Email: jorged.encyso@gmail.com


