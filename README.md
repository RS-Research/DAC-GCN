# DAC-GCN: Dual Actor-Critic Graph Convolutional Network

Welcome to the **DAC-GCN** repository! This repository contains the code implementation and related resources for the research paper:

**"DAC-GCN: A Dual Actor-Critic Graph Convolutional Network with Multi-Hop Aggregation for Enhanced Recommender Systems."**

## Description
DAC-GCN is a novel framework designed to address the critical challenges in modern recommender systems, including:
- **Data Sparsity**: Enhances recommendations with limited user-item interaction data.
- **Dynamic Preferences**: Adapts to evolving user behaviors.
- **Long-Range Dependencies**: Captures complex relationships using multi-hop graph aggregation.
- **Training Stability**: Optimizes recommendation policies and value estimation with a dual Actor-Critic architecture.

The model combines Graph Convolutional Networks (GCNs) and Reinforcement Learning (RL) techniques to improve recommendation accuracy, ranking quality, and adaptability. It leverages:
- Multi-Hop Aggregation: For capturing higher-order user-item interactions.
- Attention Mechanisms: To dynamically prioritize critical relationships.
- Dual Actor-Critic Networks: For specialized learning of policy generation and value estimation.

## Features
- **Dual Actor-Critic Architecture**: Separate networks for policy optimization and value estimation.
- **Multi-Hop Aggregation**: Models both local and global user-item interactions.
- **Attention Mechanism**: Dynamically weights important user-item interactions.
- **Benchmark Testing**: Evaluated on datasets like MovieLens, Amazon, and ModCloth.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/RS-Research/DAC-GCN.git
   cd DAC-GCN
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure Python 3.8+ and PyTorch are installed.

## Usage

### Data Preparation
Download benchmark datasets such as MovieLens, Amazon, and ModCloth from [RecBole Dataset List](https://recbole.io/dataset_list.html) and place them in the `data/` directory. The folder structure should look like:

```plaintext
data/
├── ml-100k/
│   ├── ratings.csv
│   ├── users.csv
│   └── items.csv
├── amazon-subscription-boxes/
│   ├── interactions.csv
│   └── metadata.csv
└── ...
```

### Model Training
1. Preprocess the dataset:
   ```bash
   python preprocess.py --dataset ml-100k
   ```

2. Train the DAC-GCN model:
   ```bash
   python train.py --config configs/ml-100k.yaml
   ```

3. Evaluate the model:
   ```bash
   python evaluate.py --checkpoint checkpoints/ml-100k_model.pth
   ```

## Results
DAC-GCN outperforms state-of-the-art recommender systems across multiple metrics:
- **Precision@10**
- **Recall@10**
- **NDCG@10**
- **MRR@10**
- **Hit@10**

Refer to the `results/` directory for detailed evaluation results.

## Citation
If you use DAC-GCN in your research, please cite the corresponding paper:

```bibtex
@article{dac-gcn,
  title={DAC-GCN: A Dual Actor-Critic Graph Convolutional Network with Multi-Hop Aggregation for Enhanced Recommender Systems},
  author={Gholamreza Zare and Nima Jafari Navimipour and Mehdi Hosseinzadeh and Amir Sahafi},
  journal={Acta Informatica Pragensia},
  year={2025},
  note={Under Review}
}
```

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgments
This work was conducted by:
- **Gholamreza Zare**
- **Nima Jafari Navimipour**
- **Mehdi Hosseinzadeh**
- **Amir Sahafi**

For questions or collaboration, please contact: [gholamrezazare@duytan.edu.vn](mailto:gholamrezazare@duytan.edu.vn).
