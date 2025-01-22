# Code, datasets for the paper “Rethinking Continual Knowledge Graph Embedding: Benchmarks and Analysis”
### Dataset
```
Data
├──FACT*
│  ├── FACT-3_2
│  ├── FACT-4_1
│  ├── FACT-3_1_1
├──PS-CKGE
│  ├── PS-CKGE-3_2
│  ├── PS-CKGE-4_1
│  ├── PS-CKGE-3_1_1
```
We restructured the FACT dataset and refer to it as FACT*. For both FACT* and our dataset, we set up three dynamic scenarios with data ratios of 3:2, 4:1 and 3:1:1 respectively.
### Reproduce PS-CKGE benchmarks
To construct a single-update CKGE benchmark with pattern shifts, create subfolders named `0`, `1`, and run：
```sh
python construct_1_update.py --instance_name <instance_file> --data_name <dataset_name> --ratio <data_ratio>

```
`<data_ratio>` represents the ratio of the number of triples in the initial snapshot and the number of newly added triples during each update which can be set to `4:1` or `3:2`.

To construct a double-update CKGE benchmark with pattern shifts, create subfolders named `0`, `1`, `2`, and run：
```sh
python construct_2_update.py --instance_name <instance_file> --data_name <dataset_name>

```

### Reproduction of experimental results
To reproduce the experimental results of CKGE method LKGE, the souce code of [LKGE](https://github.com/nju-websoft/LKGE) can be directly used.
