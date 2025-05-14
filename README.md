# 🧪 IMDB MOVIE Sentimental Analysis Prediction using BERT-Large

This project uses a fine-tuned **BERT-Large Uncased** model to perform text classification related to AIDS-related case studies or reports. The focus is on preprocessing the dataset, exploring the text lengths, and effectively tokenizing the data for input to the model.

## 📁 Project Structure

```
AIDS_Project/
│
├── main_code.py                # Main Jupyter notebook
|-- sentimantal_data.csv        # main data se
├── README.md                   # Project description and instructions

## 📌 Objective

To fine-tune a BERT-Large model on a dataset consisting of medical text, likely for a binary/multi-class classification task related to AIDS diagnosis, prediction, or symptom classification.

## 🛠️ Technologies Used

- 🧠 **Transformers (HuggingFace)**
- 🔢 **PyTorch**
- 🧼 **Tokenizers**
- 📊 **Matplotlib**
- 📄 **Pandas / NumPy**
- 🐍 Python 3.8+

## 📋 Key Steps in the Notebook

1. **Load BERT-Large Model & Tokenizer**  
   Using `AutoModel` and `BertTokenizerFast` from Hugging Face.

2. **Text Length Analysis**  
   Histogram plotted to visualize average sentence length.  
   → Chose **padding/truncation length = 17** based on this.

3. **Batch Tokenization**  
   All training, validation, and test text were tokenized using `batch_encode_plus` with:
   - `max_length=17`
   - `padding='max_length'`
   - `truncation=True`

4. **Preparation for Modeling**  
   The tokenized data can now be fed into BERT for classification.

## 🚀 How to Run

### 1. Clone the Repo
```bash
[git clone cd AIDS_Project](https://github.com/Chandan01097/Sentiment_analysis-NLP-project-on-IMDB-data-set)
```

### 2. Run the Notebook
Launch Jupyter or VS Code to open and run `AIDS_Project.ipynb`.

## 📈 Sample Output

- Tokenization results
- Histogram of input text lengths
- Prepared `input_ids` and `attention_mask` tensors for training

## ✅ Future Improvements

- Add model training and evaluation code.
- Integrate with Streamlit or Flask for a web interface.
- Deploy the model using Hugging Face Spaces, Heroku, or AWS Lambda.

