Task 1 – News Topic Classifier Using BERT 
Objective Fine-tune a BERT transformer model to classify news headlines into four topic categories using the AG News dataset from Hugging Face.
Dataset AG News Dataset – Available directly via Hugging Face Datasets ( ag_news ). Contains 120,000 training and 7,600 test news headlines across 4 classes: World, Sports, Business, Sci/Tech. 
Methodology / Approach 1. Loaded the AG News dataset using the Hugging Face datasets library2. Tokenized text using bert-base-uncased tokenizer with truncation and padding at max length 128 3. Used a subset of 5,000 training and 1,000 test samples for efficient Colab training 4. Fine-tuned BertForSequenceClassification with 4 output labels for 3 epochs 5. Evaluated using Accuracy and Weighted F1Score after each epoch 6. Saved the best model checkpoint and deployed via a Gradio web interface 
How to Run on Google Colab !pip install transformers datasets gradio scikit-learn torch Then upload and run task1_bert_news_classifier.py , or paste code cells into a notebook. 
Key ResultsMetric Accuracy Score ~93% F1 Score (Weighted) ~93% Results may vary slightly based on random seed and hardware.
Deployment The script launches a Gradio interface with a public shareable link. Users can type any news headline and get the predicted category along with confidence scores for all four classes. 
Skills Demonstrated NLP with Hugging Face Transformers Transfer learning and fine-tuning BERT Text classification evaluation metrics Gradio-based model deployment
