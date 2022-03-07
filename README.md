# LSTM-and-XG_boost-
LSTM and XG-Boost for NLP

## Data Cleaning and Normalization

In Natural language Processing, the crucial task is to clean the data and create clean corpus data for the training model.
The main data cleaning techniques were used here to clean the messy data are:

	1. Lower Case: This is the simplest way to normalize the text. In the end of we do have some semantic implications. 
	2. Remove Stop words. By removing the stop words we remove the low-level information from the text to focus on important information.  
	3. Remove punctuations. While training an NLP model, helps to reduce overfitting by removing punctuation.  
	4. Remove words less than length 2. Removing less than 2 length words will help to focus on the main content of the data.

In LSTM, the bag-of-words approach used to create building blocks of data from raw text helps to create a vocabulary. Vocabulary refers to the set of unique tokens in the corpus. The bag-of-words technique where we assigned numerical values to each word. Here we consider max padding length is equal to 256 for simplicity purposes (we can also consider the maximum length of the sentence in a dataset)

## Trained models on:

    1) XGBoost Algorithm
    2) Long Short-Term Memory (LSTM)
    
### XGBoost Algorithm

The decision-based ensemble machine learning algorithm XGBoost (eXtreme Gradient Boosting) helps to classify text data from the document. It uses a gradient boosting ensemble learner method like another tree-based algorithm. The main advantage of the XGBoost is that it always gives more importance to functional space when reducing the cost of the model, while other tree-based models like Random forest try to give more preference to hyperparameter tuning to optimize the model. 
Regardless of other machine learning algorithms, XGBoost takes an upper hand while executing the model. The key advantage of XGBoost is it is fast, Memory efficient, and provides high accuracy. Boosting assemble technique perform such that, new models are added to correct the errors made by existing models. Models are added sequentially until no further improvement can be made. The gradient approach is where new models are created that predict the residuals or error of prior models and then added together to make the final prediction. This approach helps in classifying text problems.
 
### Long Short-Term Memory (LSTM)

The Long Short-Term Memory (LSTM) structure solves the long-term dependencies in neural network problems. The key feature of the LSTM’s is to remember information for a long period of time and work on a large variety of data problems. 
LSTM structure is composed of Forget gate, input gate, cell state, output state.

Also, each LSTM unit has an internal memory state called “cell state” and has regulators called “gates” to control the flow of information. It can remove or add information to the state, sensibly regulated by gates. 

    1. Forget Gate
    2. Input Gate
    3. Cell State
    4. Output Gate

The Forget Gate is responsible for deciding which information is kept for calculating the cell state and which is not relevant and can be discarded. It has 2 input functionality; one is information from the previous hidden state (Previous Cell) and the information from the current cell.
Input gate updates the cell state and decides which information is important and which is not. As forget get helps to discard the information while the input gate helps to find out information and store certain data in the memory that are relevant. 
The gathered information was used to calculate the new cell state. The cell state has the capability that store and load information. The incorporated data from the previous step get passed on to the next step.
The last output gate decides what the next hidden state should be. The output of the forget gate tells the cell state which information to forget by multiplying 0 to a position in the matrix. If the output of the forget gate is 1, the information is kept in the cell state

Based on the results and the characteristics of the model, the conclusion of this task summarizes below. 

Above-stated all the models have their characteristics and they perform well in their playground. The model trained on 20000 subsamples with same batch size of test 32 and train 16 for 100 iterations.
