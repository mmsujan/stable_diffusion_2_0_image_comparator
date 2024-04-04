## Installation

 - Clone "stable_diffusion_2_0_image_comparator"
 - Open Anaconda prompt
 - cd to "stable_diffusion_2_0_image_comparator" directory
 
Run following command to create conda environment
 
```
conda env create -f environment.yaml
conda activate sd2
pip install -e .
cd stable_diffusion
pip install -r requirements.txt
```

## Run Test
 - Copy Stable Diffusion 2.0 models from [SD_2.0_models](https://intel-my.sharepoint.com/:f:/p/mohammad_sujan_miah/EuHvbZbJjfJBm3Ir3OHpOXABQjptY_GaK11kwdYfkN4gPA?e=j9pQ9Q) 
 - Unzip " models" directory and put it inside "stable_diffusion_2_0_image_comparator/stable_diffusion"
 - From conda prompt, cd path to "stable_diffusion_2_0_image_comparator/stable_diffusion" directory  
 
 Sample Run: 
 ```
 python image_compare.py
 ```
 
 - You can set different threshold values as per requirement. For an example:
 ```
 python image_compare.py --thresholds 15.0 10.0 5.0
 ```
 - Command line argument options:
 
```
usage: image_compare.py [-h] [--thresholds [THRESHOLDS [THRESHOLDS ...]]] [--correlation_const CORRELATION_CONST]
                        [--platform PLATFORM] [--verbosity]

optional arguments:
  -h, --help            show this help message and exit
  --thresholds [THRESHOLDS [THRESHOLDS ...]]
                        Maximum difference between two pixel.
  --correlation_const CORRELATION_CONST
                        When a threshold value is small, corelation constant should be higher
  --platform PLATFORM   Platform: DG2 or MTL
  --verbosity           Print error details
 
```