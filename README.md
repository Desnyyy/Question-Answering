# **Project description**
This project focus on developing an automated end-to-end Q&A system, with the ability to answer a question with any content. The system we install in this project includes two main parts: Retriever and Reader, with the goal of building a comprehensive system capable of extracting information from text and providing answers to questions. based on the content of the paragraph
literature.\
Specifically, a program based on the SQuAD2.0 dataset was built, a reading comprehension dataset, the vector database FAISS and the BERT model to perform specific tasks in the program. The input and output of the program are as follows:
* Input: a question
* Output: Corresponding answer
### **Dataset description**
SQuAD2.0 Stanford Question Answering Dataset (SQuAD) is a data set towards reading comprehension, including different passages on many topics, each passage will have a short question attached.\
Answers to short questions are words/phrases available in the given passage (no complex reasoning required), or questions that cannot be answered based on the passage (answer is no answer).\
### **Reader: DistilBERT**
1. Install and import bibraries
2. Setup config
3. Setup Dataset
4. Tokenize Dataset
* Tokenize train set: The preprocess_training_examples function takes training data as input and preprocesses it to prepare it for training the question-and-answer model. During this process, the function extracts the question list, encodes the input information with a tokenizer, and extracts offset_mapping and sample_map to map the encoded word location to the original text. The function also determines the starting and ending positions of the response in the context and adds information about this position to the inputs variable.
* Tokenize val set: We will do the same with the val set, the preprocess_validation_examples function performs data preprocessing for the model evaluation process. The function prepares a list of questions, encoding the questions and related text using a tokenizer. Then define a reference example for each input line and adjust the offset mapping to remove offsets that do not match the sequence_ids. Finally, more information about the example
reference to input.
5. Train model
6. Evaluate model
