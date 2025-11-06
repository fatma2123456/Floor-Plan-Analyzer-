# Floor Plan Analyzer 🏗️

An AI-powered tool for analyzing architectural floor plans using the Qwen2-VL vision-language model. This project enables automated extraction of dimensions, room counts, and architectural features from floor plan images.

## Features

- 🔍 **Automated Analysis**: Extract key information from floor plan images
- 📏 **Dimension Detection**: Identify plot width, depth, and total area
- 🏠 **Room Counting**: Count bedrooms, bathrooms, and other spaces
- 🚗 **Parking Analysis**: Detect number of parking spaces
- 🌳 **Outdoor Features**: Identify lawn areas and flower beds
- 💬 **Interactive Mode**: Ask custom questions about any floor plan
- 📄 **Report Generation**: Automatic summary report in text format

## Requirements

- Python 3.8+
- Google Colab (recommended) or local GPU setup
- Hugging Face account and token
- CUDA-compatible GPU (for optimal performance)

## Installation

```bash
# Install required packages
pip install -q git+https://github.com/huggingface/transformers
pip install -q qwen-vl-utils
pip install -q torch torchvision pillow accelerate
```

## Setup

1. **Hugging Face Authentication**
   
   Replace the placeholder token in the code:
   ```python
   token = "your_huggingface_token_here"
   ```
   
   Get your token from: https://huggingface.co/settings/tokens

2. **GPU Check**
   
   The script automatically detects and uses available CUDA devices. It will fall back to CPU if no GPU is available.


### Interactive Mode

After the automated analysis, you can ask custom questions:

```
Your question: Does this floor plan include a balcony?
Answer: [AI response]

Your question: What is the kitchen layout?
Answer: [AI response]

Your question: exit
```

Type `exit` to quit interactive mode.

## Output

The script generates a comprehensive report saved as `floor_plan_analysis.txt` containing:
- Image filename
- Full architectural analysis
- Answers to all predefined questions
- Structured summary format

## Model Information

- **Model**: Qwen2-VL-2B-Instruct
- **Developer**: Qwen Team / Alibaba Cloud
- **Type**: Vision-Language Model
- **Precision**: float16 (for efficiency)
- **Source**: [Hugging Face Model Hub](https://huggingface.co/Qwen/Qwen2-VL-2B-Instruct)

## Example Questions

You can ask questions like:
- "How many windows are shown in the living room?"
- "Is there a master bedroom with ensuite bathroom?"
- "What is the orientation of the main entrance?"
- "Are there any terraces or outdoor spaces?"
- "What is the approximate size of the kitchen?"



## License

This project uses the Qwen2-VL model. Please refer to the [model's license](https://huggingface.co/Qwen/Qwen2-VL-2B-Instruct) for terms of use.

## Contributing

Contributions are welcome! Areas for improvement:
- Support for batch processing multiple floor plans
- Enhanced dimension extraction algorithms
- Export to structured formats (JSON, CSV)
- Web interface integration
- Comparison tool for multiple floor plans
