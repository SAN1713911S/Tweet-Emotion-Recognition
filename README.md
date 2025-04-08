# 📊 Tweet Emotion Recognition with TensorFlow

This project focuses on building a deep learning model capable of recognizing emotions expressed in tweets using Natural Language Processing (NLP) techniques and TensorFlow. The model was trained using the [Tweet Emotion Dataset](https://github.com/dair-ai/emotion_dataset), which contains short tweets labeled with one of six emotions: anger, fear, joy, love, sadness, or surprise.

To start, all necessary libraries were installed, including TensorFlow, Hugging Face’s `datasets`, and various data visualization and preprocessing tools. Utility functions were defined to visualize training history and confusion matrices, which helped interpret the model’s performance later on.

The dataset was loaded and split into training, validation, and test sets using Hugging Face’s `load_dataset` method. Each tweet was then preprocessed by extracting its text and converting its associated label from numeric to text format. Dictionaries were created to map emotions to indices and vice versa, enabling label conversion throughout the pipeline.

For text processing, tweets were tokenized using Keras’ `Tokenizer`, transforming raw text into sequences of integers. These sequences were padded to a fixed length to ensure consistency in input shape for the neural network.

The model architecture consisted of an embedding layer followed by two bidirectional LSTM layers, a dropout layer for regularization, and two dense layers, the final one using softmax activation to output class probabilities. The model was compiled with the Adam optimizer and trained using sparse categorical crossentropy as the loss function. Early stopping was implemented to avoid overfitting.

Training was conducted over several epochs, and the model achieved a training accuracy above 98% and a validation accuracy above 93%. Once trained, the model was evaluated on the test set, reaching a final accuracy of **91.84%**.

To assess the results, training and validation metrics were visualized, a confusion matrix was plotted, and individual predictions were compared to their true labels. An example showed the model correctly predicting "anger" for a tweet about feeling frustrated and angry.

## ✅ Conclusion

This project demonstrates the effectiveness of deep learning techniques, particularly bidirectional LSTM networks, in processing and classifying emotional content in short social media texts. Achieving over 91% test accuracy, the model shows strong generalization and robustness. The entire pipeline — from data loading and preprocessing to model training and evaluation — forms a solid foundation for future advancements such as multi-label classification, sentiment intensity detection, or real-time emotion analysis in social platforms.
