---
lang: en-US
---

# NERF-ZEMAX

## Installation

Clone the repository and install the dependencies:

``` toml
install_requires =
    matplotlib >= "3.7"
    numpy >= "1.25"
    pyyaml >= "6.0"
    nerfstudio >= "0.3.1"
    torch >= "2.0.1+cu118"
    scipy >= "1.10.1"
```


## Run the script

With an environment that contains all the dependencies, run the script:

``` sh
python gui.py
```


It is import that the config file is in the directory `./data/config_test.yml`.

## Config

We can modify the default config that `gui.py` uses to run the program. The config file is a YAML file that contains the following parameters:

``` yaml
Ray file: data/mapping_simple_the_true_pinhole.txt # Ray file for 1 micro-lens
Nerf file: C:\outputs\test_bureau_2\nerfacto\2023-09-16_153142\config.yml # File containing yaml for the NERF
Output file: test_extended.sdf  # Output file
Extended ray file: data/microlensxperia9875.dat # File to extend microlens for our
Working directory: C:\\ # Reference directory for NerfStudio
Scale: 0.0075 # Scale factor between NERf and Lens Model
Reference pose: '0276' # Reference Pose
Z translation: 3 # Z translation from the reference pose
Y translation: -25 # Y translation from the reference pose

X translation: -15 # X translation from the reference pose
Z rotation: 3 # Z translation from the reference pose
Y rotation: -25 # Y translation from the reference pose
X rotation: -15 # X translation from the reference pose
Factor: 9945 # Number of rays to compute at once by the NERF. Revert to 1 if there is any issues
```