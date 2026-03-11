Final-Capstone-Project

AI Powered Product Review Comparison & Recommendation System

Domain: E-commerce / Retail Analytics

Problem Definition:
The increasing volume of online product reviews makes it difficult for customers to efficiently compare products and make informed purchasing decisions. This project aims to develop an AI-Powered Product Review Comparison & Recommendation System that uses deep learning–based sentiment analysis and generative AI to automatically analyze customer reviews. The system is trained on a publicly available Amazon review dataset and accepts real-time user-provided reviews to compare products and generate clear, intelligent recommendations, helping users choose the most suitable product.

Features Covered: Uses Kaggle Amazon Fine Food Reviews dataset (offline training), Includes proper preprocessing, Accepts real-time user-provided reviews, Compares two products, Performs sentiment analysis, Generates recommendation decision, Uses Deep Learning + Generative AI (Hugging Face)

Models Used: 1) DistilBERT → Sentiment Analysis (Deep Learning Classification Model), 2) T5 (Text-to-Text Transfer Transformer) → Natural Language Recommendation Generation (Generative AI Model)

DistilBERT is used to perform sentiment analysis on customer reviews, as it is optimized for text classification tasks and provides reliable sentiment predictions.
Although T5 can be prompted to perform sentiment analysis, it is primarily designed for text generation and sequence-to-sequence tasks rather than classification. When used for sentiment detection without fine-tuning, it can produce inconsistent or less accurate results.
Therefore, this system uses DistilBERT for accurate sentiment prediction and T5 for generating a natural language explanation and recommendation, combining both discriminative and generative AI approaches.

Dataset: Amazon Fine Food Reviews (Kaggle). This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years (~500,000 reviews). Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories. Amazon does not legally or technically allow direct access to real-time customer reviews for academic or ML training purposes. Direct use of real-time Amazon reviews is restricted due to legal, ethical, and reproducibility concerns. Therefore, the model is trained on publicly available datasets and accepts real-time user-provided reviews during inference. Companies use licensed or proprietary data sources, which are not accessible for academic projects.


The DistilBERT sentiment classification model achieved an accuracy of 92.8% on the validation dataset. The model also achieved a precision of 95.75%, recall of 95.86%, and an F1-score of 95.81%, indicating excellent performance in identifying positive and negative product reviews. Early stopping was used to prevent overfitting, and the model converged after approximately 1.4 epochs.

BLEU (Bilingual Evaluation Understudy) score is used to evaluate the similarity between the generated recommendation and a reference sentence. The score ranges from 0 to 1, where higher values indicate better similarity. The proposed system achieved a BLEU score of 0.516, indicating good quality generated recommendations from the T5 model.

Conclusion: 
The system first uses a fine-tuned DistilBERT model to perform sentiment analysis on customer reviews and compute sentiment scores for each product. The product with the higher sentiment score is selected as the recommended option. A T5 generative model then produces a natural language explanation for the recommendation. The sentiment classifier achieved 92.8% accuracy, and the text generation component achieved a BLEU score of 0.516, indicating good quality generated explanations.
