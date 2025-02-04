# Rethinking Continual Knowledge Graph Embedding: Benchmarks and Analysis
Code, datasets for the paper “Rethinking Continual Knowledge Graph Embedding: Benchmarks and Analysis”.
### Dataset
```
data
├──FACT_star
│  ├── FACT_star-3_2
│  ├── FACT_star-4_1
│  ├── FACT_star-3_1_1
├──PS-CKGE
│  ├── PS-CKGE-3_2
│  ├── PS-CKGE-4_1
│  ├── PS-CKGE-3_1_1
```
The PS-CKGE benchmark and the reconstructed FACT* benchmark, with aligned update ratios of 3:2, 4:1, and 3:1:1, are organized in the [data](https://github.com/AAnonymousName/CKGE-Benchmark/edit/main/data) repository.
### Reproduce your own PS-CKGE benchmarks
Create a folder in the `data/PS-CKGE/mybench`, `mybench` can be replaced by your own benchmark name.

To construct a single-update CKGE benchmark with pattern shifts, create subfolders named 0, 1 under `data/PS-CKGE/mybench`, and run in the [RuleC](https://github.com/AAnonymousName/CKGE-Benchmark/edit/main/RuleC) repository：
```sh
python construct_1_update.py --instance_name rule_instances.txt --data_name mybench --ratio <data_ratio>

```
`<data_ratio>` represents the ratio of the number of triples in the initial snapshot and the number of newly added triples during each update which can be set to `4:1` or `3:2`.


To construct a double-update CKGE benchmark with pattern shifts, create subfolders named 0, 1, 2 under `data/PS-CKGE/mybench`, and run in the [RuleC](https://github.com/AAnonymousName/CKGE-Benchmark/edit/main/RuleC) repository：
```sh
python construct_2_update.py --instance_name rule_instances.txt --data_name mybench

```
