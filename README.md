# Financial-Sentiment-Analysis
Financial news headlines are a fertile source of NLP data, especially when it comes to predicting how a stock will perform. Frequently, this is done via sentiment analysis, an NLP task that buckets phrases into positive, negative, and neutral. 

What is FinBERT? 
FinBERT is a pre-trained NLP model based on BERT, Google's revolutionary transformer model. Simply put: FinBERT is just a version of BERT trained on financial data (hence the "Fin" part of its name), specifically for sentiment analysis. 
Remember: BERT is a general language model. Financial news and stock reports often involve a lot of domain-specific jargon (there's plenty in the Table above, in fact), so a  model like BERT can't generalize well in this domain.


The Importance Of Sentiment Analysis in Finance ML
Sentiment analysis, meanwhile, is a very common task in NLP that aims to assign a "feeling" or an "emotion" to text. Typically, it predicts whether the sentiment is positive, negative, or neutral.
You often see sentiment analysis around social media responses to hot-button issues or to determine the success of an ad campaign. But it's promising in the financial domain as changes in sentiment around a company could help predict a rise or fall in that company's stock. 

Downloading the Stock Market News Data from Kaggle
We want to take the fine-tuned FinBERT model but put it to the test on a different dataset. For this experiment, we'll use the "Daily Financial News for 6000+ Stocks" from Kaggle.  


we'll use NumPy to shuffle the entries and convert them to a normal Python list containing the headlines. This list can be used as an input to the FinBERT model. 
Then, from the HuggingFace Model Hub, we'll download the pre-trained tokenizer, which is used to convert text into tokens that NLP models can understand. We also load the pre-trained model itself in a similar way. 

Running Inference with FinBERT and Stock Market News Headlines
We can take the Python list of the headlines we've preprocessed (note: yes, tokenizer accepts Python lists of strings as input), and pass them through the tokenizer to preprocess them before being inputted into the model with the following lines of code.

Visualizing the Results Interactively as a W&B Table
W&B Tables is an awesome Weights & Biases feature that lets interactively visualize and explore tabular data. And it is extremely easy to create one. 
All we need to do is define a Pandas DataFrame (basically, defining a table in Python) with the four relevant to us columns.  

Visualizing the W&B Table
we've logged the Table, it will start a new run in our project and print something like this in the console. We can click on this "Run page" link to open our Run Page dashboard and see the W&B Table we've created. 
<img width="1137" alt="image" src="https://github.com/RohitSharma0719/Financial-Sentiment-Analysis/assets/42697628/939a3008-bede-4966-bdaa-b7371c041c6b">

<img width="1343" alt="image" src="https://github.com/RohitSharma0719/Financial-Sentiment-Analysis/assets/42697628/b3f40c4c-148c-438a-a912-dc281d3d0b90">

