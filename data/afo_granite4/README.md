### ROCM pytorch Tunable Ops files

to run granite-4 on Strix Halo

Also set the following environment variables in the docker containers after copying the files in this directory into the container's `/opt/afo_granite4` directory

```
PYTORCH_ROCM_ARCH='gfx90a;gfx942;gfx950;gfx1100;gfx1101;gfx1151;gfx1200;gfx1201'
PYTORCH_TUNABLEOP_ENABLED=1
PYTORCH_TUNABLEOP_FILENAME=/opt/afo_granite4/afo_tune_device_%d_full.csv
PYTORCH_TUNABLEOP_TUNING=0
SAFETENSORS_FAST_GPU=1
TOKENIZERS_PARALLELISM=false
VLLM_V1_USE_PREFILL_DECODE_ATTENTION=0
```
