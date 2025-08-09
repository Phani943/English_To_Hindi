# English to Hindi Neural Machine Translation

A deep learning-based neural machine translation system that translates English text to Hindi using a sequence-to-sequence LSTM architecture.

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 🚀 Features

- **High Accuracy Translation**: Achieves 97% validation accuracy
- **Robust Architecture**: Encoder-decoder LSTM model
- **Large Vocabulary**: Supports 52K+ English and 62K+ Hindi words
- **Pre-trained Models**: Ready-to-use tokenizers and model checkpoints

## 🏗️ Model Architecture

The translation system uses a **sequence-to-sequence (seq2seq)** architecture:

- **Encoder**: LSTM layer that processes English input sequences
- **Decoder**: LSTM layer that generates Hindi output sequences  
- **Embedding Layers**: 440-dimensional embeddings for both languages
- **Output Layer**: Dense layer with softmax activation

## 📊 Dataset

- **Source**: English-Hindi parallel corpus from Kaggle
- **Size**: 80,000 sentence pairs
- **Languages**: English → Hindi translation pairs
- **Preprocessing**: Tokenization, sequence padding, and special token handling

## 🛠️ Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/Phani943/English_To_Hindi.git
    cd English_To_Hindi
    ```

2. **Install dependencies**
    ```bash
    pip install tensorflow keras numpy pandas matplotlib seaborn jupyter
    ```

3. **Additional requirements for full functionality**
    ```bash
    pip install scikit-learn pickle-mixin
    ```

### Training Your Own Model

Open and run the Jupyter notebook:

```bash
jupyter notebook notebook/encoder-decoder-final.ipynb
```

## 📁 Project Structure

```
English_To_Hindi/
├── notebook/
│   └── encoder-decoder-final.ipynb   # Main training notebook
├── pickles/
│   ├── eng_tokenizer.pkl              # English tokenizer
│   └── hindi_tokenizer.pkl            # Hindi tokenizer
├── config.json                        # Model configuration
└── README.md                          # Project documentation
```

## ⚙️ Configuration

`config.json` contains key model parameters:

```json
{
    "eng_max_len": 100,
    "hindi_max_len": 300,
    "latent_dim": 440,
    "eng_vocab_size": 52648,
    "hindi_vocab_size": 62705
}
```

## 📈 Model Performance

- **Training Epochs**: 9 (with early stopping)
- **Final Validation Accuracy**: ~97%
- **Loss Reduction**: 0.60 → 0.13
- **Architecture**: Encoder-Decoder LSTM
- **Vocabulary Coverage**: 52K+ English, 62K+ Hindi words

## 🔧 Technical Specifications

| Component            | Specification      |
|----------------------|--------------------|
| **Framework**        | TensorFlow/Keras   |
| **Architecture**     | Seq2Seq LSTM       |
| **Embedding Dim**    | 440                |
| **Max Sequence Len** | EN: 100, HI: 300   |
| **Vocabulary Size**  | EN: 52,648, HI: 62,705 |
| **Special Tokens**   | `<sos>`, `<eos>`, `<unk>` |

## 🚦 Getting Started

1. **Explore the notebook**: Start with `notebook/encoder-decoder-final.ipynb`
2. **Understand the data**: Review preprocessing steps and data analysis
3. **Load pre-trained components**: Use the tokenizers in `pickles/` folder
4. **Experiment**: Modify hyperparameters in `config.json`
5. **Train your model**: Run the complete training pipeline

## 🤝 Contributing

Contributions are welcome! Please follow the steps:

1. Fork the repository  
2. Create your feature branch:  
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your changes:  
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. Push to the branch:  
   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a Pull Request

## 📝 Future Enhancements

- Implement transformer architecture
- Add BLEU score evaluation
- Create web interface for real-time translation
- Support for longer sequences
- Batch translation functionality
- Model quantization for mobile deployment

## 📧 Contact

**Phani Chaitanya**  
📩 [phanichaitanya63@gmail.com](mailto:phanichaitanya63@gmail.com)  

Project Link: [https://github.com/Phani943/English_To_Hindi](https://github.com/Phani943/English_To_Hindi)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ **Star this repository if you found it helpful!**
