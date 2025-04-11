# AI Security Research and Applications

This repository contains implementations of AI security research focusing on data poisoning attacks and defense mechanisms, along with the accompanying research paper.

## 📑 Research Paper

**The Evolving Landscape of Artificial Intelligence Security: A Comprehensive Review of Vulnerabilities and Defense Mechanisms**

Our research paper examines recent advances and vulnerabilities in AI security, with particular focus on:
- Data poisoning in code generation
- Vulnerability handling in AI-generated code
- Adversarial attacks on explainable AI systems
- Analysis of practical security incidents

Key findings reveal that pre-trained models are particularly susceptible to data poisoning attacks, with as little as 3% of malicious training data potentially compromising up to 41% of generated outputs.

[Read the full paper](./research/paper.pdf)

## 🔧 Applications

### 1. MNIST Evasion Attack Demo

A demonstration of evasion attacks on the MNIST dataset using adversarial perturbations.

#### Prerequisites
- Python 3.x
- Google Colab account
- SecML library

#### Installation
```bash
pip install git+https://github.com/pralab/secml
```

#### Usage
1. Open the provided Jupyter notebook in Google Colab
2. Follow the step-by-step implementation in the notebook
3. Experiment with different perturbation parameters

[Go to MNIST Demo](./mnist-demo)

### 2. Face Recognition Attack Demo

An implementation of data poisoning attacks on face recognition systems using adversarial patches.

#### Prerequisites
- Python 3.x
- TensorFlow/Keras
- OpenCV
- Pillow
- NumPy
- Matplotlib

#### Installation
```bash
pip install tensorflow opencv-python pillow numpy matplotlib tqdm
```

#### Usage

Generate an adversarial patch:
```bash
python generate_patch.py <scale_factor> <output_file>
```

Poison the dataset:
```bash
python poison_data_class.py <adversarial_patch_path> <input_dir> <output_dir>
```

Run the demo:
```bash
python feed.py [model_file=model.keras] [device_id=0] [tolerance=0.99]
```

[Go to Face Recognition Demo](./face-recognition-demo)

## 📊 Results

Our implementations demonstrate:
- Successful evasion attacks on MNIST with high accuracy degradation
- Effective data poisoning in face recognition systems
- Practical application of theoretical attack vectors
- Real-world implications for AI security

## 🛡️ Security Considerations

This repository is for educational and research purposes only. The implementations demonstrate vulnerabilities to improve understanding and develop better defense mechanisms. Do not use these techniques on production systems or without explicit permission.

## 📖 Citation

If you use this work in your research, please cite:
```bibtex
@article{ahlal2024evolving,
  title={The Evolving Landscape of Artificial Intelligence Security: A Comprehensive Review of Vulnerabilities and Defense Mechanisms},
  author={Ait Ahlal, Mouaad},
  journal={ENSA Berrechid, Hassan Premier University},
  year={2024}
}
```

## 🤝 Contributing

Contributions are welcome!

## 👥 Authors

- **Mouaad AIT AHLAL** - *Initial work* - [ENSA Berrechid, Hassan Premier University]
- Farid Elidrissi Rajaa
- El Far Moad
- Lakrafi Oussama

## 🔗 Links

- [Research Paper](./research/paper.pdf)
- [MNIST Demo](./mnist-demo)
- [Face Recognition Demo](./face-recognition-demo)
- [Projects guide](./guide/guide.pdf)

## 🙏 Acknowledgments

- Dr. Hnini Abdelhalim for project supervision
- Dr Saul Johnson (previously at NHL Stenden) for his impressive and inspiring data poisoning python project
