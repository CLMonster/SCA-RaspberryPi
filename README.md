# SCA-RaspberryPi-EM-datasets

This repository contains electromagnetic trace data from the Raspberry Pi 2B, as presented in our paper *"Attacking High-Performance SBCs: A Generic Preprocessing Framework for EMA"*.

## Acquisition Settings

The acquisition methods and devices used for trace collection are detailed in our paper.

## Download Link

The dataset is approximately 15 GB in size. You can download it using the following link:

[Download Link](https://pan.baidu.com/s/1Dn4Kt-677sxwpa_3p0wHYg)  
Password: `9ivm`

## How to Use It?

The dataset is provided in the `.ets` file format, which was created by the eShard team. We recommend using the [estraces](https://github.com/eshard/estraces) library to process the data.

### Install `estraces`:

```bash
pip install estraces
```

### Convert `.ets` file into a NumPy array:

```python
import estraces

# Read the .ets file
ths = estraces.read_ths_from_ets_file("xxx.ets")
print(ths[0])

# Access the samples (as a NumPy ndarray)
samples = ths.samples[:]  # type: numpy.ndarray

# Access all metadata associated with the traces
print(ths.metadatas)  # dict-like object
```

## References

Coming soon.
