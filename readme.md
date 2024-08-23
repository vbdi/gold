## [[NAACL 2024] GOLD: Generalized Knowledge Distillation via Out-of-Distribution-Guided Language Data Generation](https://arxiv.org/pdf/2403.19754.pdf)

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/gold-generalized-knowledge-distillation-via/data-free-knowledge-distillation-on-squad)](https://paperswithcode.com/sota/data-free-knowledge-distillation-on-squad?p=gold-generalized-knowledge-distillation-via)

<p align="center">
<img src="figures/Fig1.png?raw=true" alt="alt text" width="440" height="204">
</p> 

GOLD is a task-agnostic data generation and knowledge distillation framework, which employs an iterative out-of-distribution-guided feedback mechanism for the LLM. As a result, the generated data improves the generalizability of distilled models. An energy-based OOD evaluation approach is also introduced to deal with noisy generated data. Our extensive experiments on 10 different classification and sequence-to-sequence tasks in NLP show that GOLD respectively outperforms prior arts and the LLM with an average improvement of 5% and 14%. 

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
## Cite
```
@inproceedings{gholami-etal-2024-gold,
    title = "{GOLD}: Generalized Knowledge Distillation via Out-of-Distribution-Guided Language Data Generation",
    author = "Gholami, Mohsen  and Akbari, Mohammad  and Hu, Tianxi  and Masrani, Vaden  and Wang, Z.  and Zhang, Yong",
    booktitle = "Findings of the Association for Computational Linguistics: NAACL 2024",
    year = "2024",
}
```
