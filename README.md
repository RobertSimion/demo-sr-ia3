# Child Speech Recognition for Early-Grade Reading Assessments

**A PhD Research Project Introduction by Robert S. | UPB ETTI**  
*Supervisor: Prof. Dr. Ing. Dragoș Burileanu*

## 📋 Project Overview

This repository contains a comprehensive PhD research project focused on developing robust child speech recognition systems for educational purposes. The project addresses the significant gap between adult and child speech recognition accuracy, aiming to create automated reading assessment tools for early-grade education.

## 🎯 Research Objectives

- **General Objective**: Develop robust child ASR systems for educational purposes
- **Specific Objectives**:
  - Match adult-level accuracy for child speech recognition
  - Adapt ASR for phonics, decoding, and syllable tasks
  - Automate scoring for reading assessments
- **Expected Deliverables**:
  - Web/mobile demo application
  - Publications in top-tier conferences (Interspeech, ICASSP)

## 📊 Problem Statement

- **Current Challenge**: Existing ASR models are optimized for adults
- **Child Speech Characteristics**: Higher pitch, less fluency, unique acoustic properties
- **Performance Gap**: WER on child speech ~12–15% vs <3% for adults
- **Goal**: Automated reading assessment for educational applications

## 🏗️ Architecture & Models

The project implements and compares two state-of-the-art architectures:

### A. wav2vec2
- CNN feature extractor with 7 blocks
- Transformer BASE: 12 layers, 768-dimensional
- Gumbel softmax quantization
- Self-supervised learning approach

### B. Whisper
- Encoder-decoder transformer architecture
- 2 CNN layers for feature extraction
- 80-channel log-Mel spectrogram input
- Available in Tiny, Medium, and Large variants

## 📈 Performance Benchmarks

| Dataset | wav2vec2 WER | Whisper WER |
|---------|--------------|-------------|
| MyST | 7.42% | 12.28% |
| PFSTAR | 2.91% | 2.98% |
| CMU-Kids | 12.77% | 15.08% |

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- CUDA-compatible GPU (recommended)
- FFmpeg for audio processing

### 1. Clone the Repository
```bash
git clone <repository-url>
cd demo-sr-ia3
```

### 2. Create Virtual Environment
```bash
# Create virtual environment
python -m venv .venvspeech

# Activate virtual environment
# On Windows:
.venvspeech\Scripts\activate
# On macOS/Linux:
source .venvspeech/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Install Additional System Dependencies
- **Windows**: Install Visual C++ Redistributable
- **macOS**: Install Xcode command line tools
- **Linux**: Install build-essential and audio libraries

## 🚀 Running the Notebook

### 1. Start Jupyter Notebook
```bash
jupyter notebook
```

### 2. Open the Main Notebook
Navigate to and open `Merged_PhD_Child_Speech_Recognition.ipynb`

### 3. Run All Cells
Execute the notebook cells sequentially to:
- Load and test speech recognition models
- Process audio data
- Evaluate model performance
- Visualize results and charts

## 📁 Project Structure

```
demo-sr-ia3/
├── .venvspeech/                    # Virtual environment
├── charts/                         # Visualization assets
│   ├── chart.png                   # Performance comparison chart
│   ├── research_workflow.png       # Research methodology diagram
│   ├── wav2vec2_architecture.png   # wav2vec2 model architecture
│   └── whisper_architecture.png    # Whisper model architecture
├── Merged_PhD_Child_Speech_Recognition.ipynb  # Main research notebook
├── requirements.txt                # Python dependencies
├── Generics.pptx                  # Presentation materials
└── .gitignore                     # Git ignore rules
```

## 🧪 Key Features

### Data Processing Pipeline
- Audio preprocessing and normalization
- Feature extraction for both wav2vec2 and Whisper
- Cross-validation and evaluation metrics

### Model Implementation
- Pre-trained model loading and fine-tuning
- Inference pipelines for both architectures
- Performance benchmarking and comparison

### Evaluation Metrics
- Word Error Rate (WER) calculation
- Cross-dataset validation
- Error analysis and visualization

## 📚 Research Methodology

The project follows a systematic 4-year research timeline:

1. **Year 1**: Literature review, dataset curation, baseline establishment
2. **Year 2**: Advanced model development and adaptation
3. **Year 3**: Romanian corpus development and transfer learning
4. **Year 4**: Deployment, application development, and publication

## 🔧 Troubleshooting

### Common Issues

1. **PyTorch Installation Issues**:
   ```bash
   pip uninstall torch torchvision torchaudio
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
   ```

2. **Audio Library Dependencies**:
   ```bash
   # Install system audio libraries
   # Ubuntu/Debian:
   sudo apt-get install libsndfile1 ffmpeg
   # macOS:
   brew install libsndfile ffmpeg
   ```

3. **CUDA Compatibility**:
   - Ensure CUDA version matches PyTorch requirements
   - Use CPU version if GPU is not available

## 📊 Expected Outputs

When running the notebook successfully, you should see:
- Model loading confirmations
- Audio processing demonstrations
- Transcription examples
- Performance metrics and visualizations
- Research workflow diagrams

## 🔬 Research Applications

- **Educational Technology**: Automated reading assessment tools
- **Speech Therapy**: Child speech development monitoring
- **Language Learning**: Pronunciation feedback systems
- **Accessibility**: Assistive technologies for children with learning difficulties

## 📞 Contact & Support

**Robert Simion**
- Email: simion.robert.florin@gmail.com,robert-florin.simion@ing.com
- Institution: UPB ETTI
- LinkedIn: https://www.linkedin.com/in/robert-simion-b25110133/
- Supervisor: Prof. Dr. Ing. Dragoș Burileanu

## 📖 References & Resources

- [wav2vec2 Paper](https://arxiv.org/pdf/2006.11477)
- [Whisper Documentation](https://huggingface.co/spaces/openai/whisper)
- [Transformers Library](https://huggingface.co/docs/transformers/model_doc/wav2vec2)
- [Neural Networks Visualization](https://www.3blue1brown.com/?v=neural-networks)

## 📝 License

This project is part of ongoing PhD research at UPB ETTI. Please contact the author for usage permissions and collaboration opportunities.

---

## 📝 More to do
