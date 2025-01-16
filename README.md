# Fashion Product Recommendation Using Multimodal Learning

This project develops an AI-driven model for **fashion product recommendation** by leveraging **multimodal learning**. The model integrates **image and text data** to classify fashion items into appropriate categories, enhancing user experience in online retail environments. By combining visual and textual features, the model provides accurate and personalized product recommendations, improving customer satisfaction and streamlining product discovery.

---

## Key Features
- **Multimodal Learning**: Combines image and text data for better product categorization.
- **Image Processing**: Uses **EfficientNetB0** for feature extraction from high-quality product images.
- **Text Processing**: Employs an **LSTM-based model** to process textual descriptions.
- **Early Fusion**: Concatenates image and text features for improved classification.
- **High Accuracy**: Achieves **91% accuracy** on a curated fashion product dataset.

---

## Dataset
The dataset used in this project is available on Kaggle:  
[Fashion Product Text & Images Dataset](https://www.kaggle.com/datasets/nirmalsankalana/fashion-product-text-images-dataset/data)
containing:
- **Images**: High-quality product images (1080 x 1440 px).
- **Text**: Titles and descriptions of products.
- **Labels**: Product categories.

**Preprocessing Steps**:
- Images resized to 224x224 px.
- Text tokenized and padded to a maximum length of 100.
- Labels encoded using one-hot encoding.

---

## Model Architecture
1. **Image Input**: Features extracted using EfficientNetB0 and processed through global average pooling.
2. **Text Input**: Tokenized text data passed through an embedding layer followed by LSTM.
3. **Fusion**: Features from both modalities concatenated.
4. **Output**: Fully connected layer with softmax activation for category classification.

**Implementation Details**:
- **Framework**: TensorFlow and Keras.
- **Optimizer**: Adam (learning rate: 0.001).
- **Loss Function**: Categorical Crossentropy.
- **Metrics**: Accuracy.

---

## Results
### Performance Metrics
| Metric          | Multimodal Model | Image-Only Model | Text-Only Model |
|-----------------|------------------|------------------|-----------------|
| **Accuracy**    | 91%              | 85%              | 87%             |
| **Precision**   | 90%              | 83%              | 86%             |
| **Recall**      | 91%              | 84%              | 86%             |
| **F1-Score**    | 90.5%            | 83.5%            | 86%             |

