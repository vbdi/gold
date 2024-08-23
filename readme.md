## [[NAACL 2024] GOLD: Generalized Knowledge Distillation via Out-of-Distribution-Guided Language Data Generation](https://arxiv.org/pdf/2403.19754.pdf)

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/gold-generalized-knowledge-distillation-via/data-free-knowledge-distillation-on-squad)](https://paperswithcode.com/sota/data-free-knowledge-distillation-on-squad?p=gold-generalized-knowledge-distillation-via)

<p align="center">
<img src="figures/Fig1.png?raw=true" alt="alt text" width="440" height="204">
</p> 

## Install dependencies:
```conda env create -f environment.yml```


## Experiments on Classification Tasks:
```
python T5_glue.py --scenario0 --num_batches 375 --data_dir generated_data/rte_ours/ --epochs 1 --generate_data  --dataset rte --fb val_ac
```

## Experiments on Seq-to-Seq Tasks:
```
python T5_squad.py --scenario1 --data_dir generated_data/svamp/ --num_batches 375 --epochs 1 --fb val_ac --dataset svamp  
```
