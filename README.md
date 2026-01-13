# Recipe Generation from Food Images

An AI-powered web application that generates cooking recipes from food images using deep learning models. The system identifies dishes, predicts ingredients, and generates step-by-step cooking instructions.

## Overview

This application uses a transformer-based neural network architecture to perform inverse cooking - generating complete recipes from food photographs. The model employs an encoder-decoder structure with multi-head attention mechanisms to predict ingredients as sets and generate cooking instructions.

## Features

- Image-based recipe generation
- Ingredient prediction
- Step-by-step cooking instructions
- Multiple recipe suggestions per image
- Recipe favorites management
- Dark mode user interface
- Sample images for testing


### Clone the Repository

```bash
git clone https://github.com/yourusername/Recipe-Generation-from-Food-Image.git
cd Recipe-Generation-from-Food-Image
```

```bash
pip install -r requirements.txt
```

The application will be accessible at `http://127.0.0.1:5000`

### Using the Application

1. **Upload an Image**: Click the upload button and select a food image from your device
2. **Use Sample Images**: Click "Try Sample Images" to test with pre-loaded examples
3. **View Results**: The system will display the dish name, ingredients list, and cooking instructions
4. **Save Favorites**: Click the heart icon to save recipes to your favorites collection
5. **Access Favorites**: Navigate to the Favorites page to view saved recipes

## Project Structure

```
Recipe-Generation-from-Food-Image/
├── Foodimg2Ing/
│   ├── data/                    # Model weights and vocabularies
│   ├── modules/                 # Neural network modules
│   ├── static/                  # CSS, JavaScript, and images
│   ├── Templates/               # HTML templates
│   ├── utils/                   # Utility functions
│   ├── __init__.py             # Flask application initialization
│   ├── args.py                 # Argument parser
│   ├── model.py                # Model architecture
│   ├── output.py               # Prediction pipeline
│   └── routes.py               # Application routes
├── requirements.txt            # Python dependencies
└── run.py                      # Application entry point
```

## Technical Details

### Model Architecture

- **Encoder**: ResNet-based convolutional neural network for image feature extraction
- **Decoder**: Transformer decoder with multi-head attention for sequence generation
- **Vocabulary**: Pre-trained vocabularies for ingredients and cooking instructions

### Processing Pipeline

1. Image preprocessing and normalization
2. Feature extraction using convolutional encoder
3. Ingredient prediction using attention mechanism
4. Recipe generation using transformer decoder
5. Post-processing and validation

