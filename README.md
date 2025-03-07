# Movie Review Sentiment Analyzer

## Project Overview
A machine learning-based sentiment analysis system that classifies movie reviews as positive or negative. This project implements concepts from text processing, feature extraction, and Support Vector Machine (SVM) classification.

## Table of Contents
- [Features](#features)
- [Technical Implementation](#technical-implementation)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)

## Features
- Text preprocessing and cleaning
- Bag-of-words feature extraction
- SVM-based classification
- Simple and efficient sentiment prediction
- Easy-to-use interface for testing reviews

## Technical Implementation
### Dependencies
```python
numpy==1.21.0
scikit-learn==1.0.2
```

### Core Components
1. **Text Preprocessing**
   - Lowercase conversion
   - Punctuation removal
   - Word tokenization
   - Basic text cleaning

2. **Feature Extraction**
   - CountVectorizer implementation
   - 1000 maximum features
   - Bag-of-words representation

3. **Classification Model**
   - Linear Support Vector Classification
   - Binary sentiment prediction
   - Optimized training parameters (2000 iterations)

## Project Structure
```
movie_sentiment_analyzer/
├── README.md
├── requirements.txt
├── src/
│   ├── preprocessor.py
│   ├── model.py
│   └── predict.py
└── examples/
    └── example_reviews.txt
```

## Installation
1. Clone the repository:
```bash
git clone https://github.com/arushimathur2604/Movie-Review-Sentiment-Analyzer.git
cd Movie-Review-Sentiment-Analyzer
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage
### Basic Usage
```python
from src.predict import predict_sentiment

# Example reviews
reviews = [
    "This movie was really great, I enjoyed every minute!",
    "Terrible waste of time, poor acting and boring plot"
]

# Get predictions
for review in reviews:
    sentiment = predict_sentiment(review)
    print(f"Review: {review}")
    print(f"Sentiment: {sentiment}\n")
```

### Example Output
```
Review: This movie was really great, I enjoyed every minute!
Sentiment: Positive

Review: Terrible waste of time, poor acting and boring plot
Sentiment: Negative
```

## Model Details
### Training Data
- Binary classification dataset
- Preprocessed text data
- Balanced positive and negative examples

### Model Architecture
- Algorithm: Linear Support Vector Classification
- Features: Bag-of-words representation
- Vector Size: 1000 features
- Training Parameters:
  - Max iterations: 2000
  - Random state: 42
  - Test split: 20%

### Performance Metrics
- Model trained on text classification dataset
- Evaluates using accuracy and confusion matrix
- Handles various text input formats

## Future Improvements
1. **Enhanced Text Processing**
   - Advanced tokenization
   - Lemmatization
   - Named entity recognition

2. **Model Improvements**
   - Cross-validation implementation
   - Hyperparameter tuning
   - Multiple classification models comparison

3. **Feature Additions**
   - Sentiment strength scoring
   - Multi-class sentiment classification
   - Web-based user interface
   - Real-time analysis capabilities

4. **Visualization**
   - Sentiment distribution plots
   - Confidence scores visualization
   - Word importance analysis

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Developed as part of machine learning coursework
- Inspired by text classification techniques and SVM implementations
- Built using concepts from FMML labs and exercises
