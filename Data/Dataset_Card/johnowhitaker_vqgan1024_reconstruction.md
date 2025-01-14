VQGAN is great, but leaves artifacts that are especially visible around things like faces. 

It's be great to be able to train a model to fix ('devqganify') these flaws.

For this purpose, I've made this dataset, which contains 100k examples, each with
- A 512px image
- A smaller 256px version of the same image
- A reconstructed version, which is made by encoding the 256px image with VQGAN (f16, 1024 version from https://heibox.uni-heidelberg.de/d/8088892a516d4e3baf92, one of the ones from taming-transformers) and then decoding the result. 

The idea is to train a model to go from the 256px vqgan output back to something as close to the original image as possible, or even to try and output an up-scaled 512px version for extra points. 

Let me know what you come up with :)

Usage:
```python
from datasets import load_dataset
dataset = load_dataset('johnowhitaker/vqgan1024_reconstruction')
dataset['train'][0]['image_256'] # Original image
dataset['train'][0]['reconstruction_256'] # Reconstructed version
````



Approximate code used to prepare this data: https://colab.research.google.com/drive/1AXzlRMvAIE6krkpFwFnFr2c5SnOsygf-?usp=sharing (let me know if you hit issues)

I'll be making a similar dataset with other VQGAN variants and posting progress on devqganify models soon, feel free to get in touch for more info (@johnowhitaker)