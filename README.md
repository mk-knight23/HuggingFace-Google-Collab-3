# Text-to-Speech Generation with LLM using Hugging Face

A simple and efficient implementation of text-to-speech generation using Hugging Face's transformers library and the Bark TTS model.

## 🎯 Project Description

This project demonstrates how to convert text into natural-sounding speech using state-of-the-art AI models. It leverages Hugging Face's transformers library and the Bark TTS model to provide high-quality audio generation from text input.

## 🚀 Features

- **Easy-to-use**: Simple pipeline-based implementation
- **High-quality audio**: Uses the Bark TTS model for natural speech
- **GPU acceleration**: CUDA support for faster processing
- **Interactive**: Built for Jupyter notebook environment
- **Minimal setup**: Few lines of code to get started

## 📋 Requirements

- Python 3.7+
- transformers library
- torch
- IPython (for audio playback in notebooks)

## 🛠️ Installation

```bash
pip install transformers torch IPython
```

## 📝 Usage

### Basic Usage

```python
from transformers import pipeline

# Initialize the TTS pipeline
pipe = pipeline("text-to-speech", model="suno/bark-small", device="cuda")

# Generate speech from text
text = "Your text here"
output = pipe(text)

# Play the audio
from IPython.display import Audio
Audio(output["audio"], rate=output["sampling_rate"])
```

### Example

The included Jupyter notebook demonstrates the complete workflow:
1. Install dependencies
2. Import required libraries
3. Initialize the TTS pipeline
4. Generate speech from sample text
5. Play the generated audio

## 🔧 Technical Details

- **Model**: suno/bark-small
- **Task**: text-to-speech
- **Device**: CUDA (GPU) recommended
- **Output**: Audio array with sampling rate

## 🎨 Customization

You can customize the implementation by:
- Changing the input text
- Using different Bark model variants
- Adjusting audio parameters
- Adding post-processing effects

## 📁 Project Structure

```
├── Text_to_speech_generation_with_LLM_with_hugging_face.ipynb
├── SUMMARY.md
├── README.md
└── index.html
```

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements.

## 📄 License

This project is open source and available under the MIT License.

## 🔗 Resources

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Bark TTS Model](https://huggingface.co/suno/bark)
- [Text-to-Speech Documentation](https://huggingface.co/tasks/text-to-speech)