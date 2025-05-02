# FashionGAN_Multimodal_Search

## Project Overview

In the dynamic world of e-commerce, finding the perfect outfit can be challenging. Traditional keyword-based searches often fall short in capturing nuanced preferences. Our project aims to revolutionize the fashion e-commerce search experience using deep learning, specifically Generative Adversarial Networks (GANs), to enhance search engine comprehension of user queries by incorporating both image and text inputs.

## Implementation Details

### Model Architecture
- **Generator**: Combines image and text features using a pre-trained BERT model for text encoding and convolutional layers for image features. Generates images from combined features.
- **Discriminator**: Classifies images as real or fake using convolutional layers and LeakyReLU activation.

### Data Preprocessing
- **Dataset**: Uses the Fashion IQ dataset containing fashion images and corresponding captions.
- **Custom Dataset Class**: FashionDataset class for loading and preprocessing image-caption pairs with BERT tokenizer.

### Training
- **Setup**: Utilizes Adam optimizer and adversarial loss function (BCELoss).
- **Training Strategies**: Includes Wasserstein GAN with gradient penalty, label smoothing, and a two-time scale update rule.

### Evaluation
- **Metrics**: Accuracy, loss, precision, recall, and F1 score are used to evaluate model performance.
- **Testing**: The model is tested on a separate test dataset to assess generalization and overall accuracy.

## Deployment

The model is deployed locally using a Language Model (LLM) Chatbot integrated into a graphical user interface (GUI) created with tkinter.

### Workflow
1. **User Interaction**: Users input text messages describing fashion items.
2. **Keyword Detection**: Chatbot detects keywords related to shopping from user messages.
3. **Image Generation**: Pre-trained generator model creates images corresponding to detected keywords.
4. **Image Display**: Generated images are displayed in the chat area of the GUI.
5. **User Feedback**: Chatbot provides feedback by displaying detected keywords and generated images.

## Benefits

- **Improved User Experience**: Provides visual representations of fashion items based on text descriptions.
- **Interactive Shopping Experience**: Creates an engaging shopping experience by generating images from user queries.

## Novelty

- **Multimodal Approach**: Combines image and text inputs for more accurate search results.
- **Conditional GANs**: Generates images that align with specific user queries.
- **SynthTriplet GAN Architecture**: Uses triplet loss for optimizing product retrieval.
- **Advanced Training Strategies**: Improves stability and quality of training.

## GUI Design

The chatbot interface features user-friendly design with distinct tabs for easy navigation, and an image upload option for sharing images within the chatbot.

## Future Work

The model requires further training to improve accuracy and generate more realistic images. A Google Colab A100 GPU has been purchased to accelerate the training process.

## Repository

- **Code**: Available in the `code` folder.
- **Comprehensive Report**: Detailed report on model architecture, training process, evaluation metrics, and performance graphs available in `report.pdf`.

For questions or feedback, please [email](mailto:gayatriwalke@gmail.com).
Thank You
