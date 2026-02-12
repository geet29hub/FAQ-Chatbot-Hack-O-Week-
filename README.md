📘 FAQ CHATBOT FOR STUDENT QUERIES
Second Year Mini Project Report
 https://colab.research.google.com/drive/1tLN9yJK4ad_H_B-0z5Lg5TYjuy6tODXi#scrollTo=IN_2e425YvZ5
1. INTRODUCTION
In educational institutions, students frequently ask repetitive questions related to admissions, fees, hostel, exams, and administration. Handling such queries manually consumes time and resources.
To solve this problem, we designed a FAQ-based chatbot using Python and Machine Learning techniques. The chatbot automatically understands student queries and provides appropriate responses using Natural Language Processing (NLP).
 
2. OBJECTIVES OF THE PROJECT
The main objectives of this project are:
• To design a chatbot that answers frequently asked questions
• To preprocess and clean student queries
• To retrieve relevant answers using TF-IDF similarity
• To classify student queries into different intents
• To provide an automated and user-friendly solution
 
3. SYSTEM REQUIREMENTS
Software Requirements:
• Python 3
• Google Colab / Jupyter Notebook
• Libraries:
o NLTK
o Scikit-learn
Hardware Requirements:
• Any computer with internet access
 
4. TASK-WISE EXPLANATION
 
🔹 TASK 1: BASIC FAQ RESPONDER
Explanation:
The basic FAQ responder uses a rule-based approach.
Each predefined question is mapped to a fixed answer using a dictionary.
When a user asks a question:
• The chatbot checks if the question exists
• If found → returns the answer
• Else → returns a default message
Implementation Concept:
• Python dictionary (key: question, value: answer)
• Direct matching
Example:
Input: What is fee structure?
Output: Fee structure is available on the official website.
 
🔹 TASK 2: PREPROCESSING STUDENT QUERIES
Why Preprocessing is Needed:
Student queries may contain:
• Capital letters
• Punctuation
• Extra words (stopwords)
• Different word forms
Preprocessing improves accuracy and consistency.
Preprocessing Steps:
1. Convert text to lowercase
2. Remove punctuation
3. Remove numbers
4. Remove stopwords (is, the, are, etc.)
5. Apply lemmatization (fees → fee)
Tools Used:
• NLTK
• Stopwords
• WordNet Lemmatizer
Example:
Original Query:
What are the hostel facilities available?
After Preprocessing:
hostel facility available
 
🔹 TASK 3: SYNONYM-AWARE FAQ BOT
Explanation:
Different students may use different words for the same meaning.
Example:
• fees → payment
• admission → enrollment
• hostel → accommodation
To handle this, WordNet is used to find synonyms.
Advantage:
• Improves understanding of semantically similar queries
• Makes chatbot more flexible
Example:
If user uses the word “payment”, chatbot understands it relates to fees
 
🔹 TASK 4: FAQ RETRIEVAL USING TF-IDF
What is TF-IDF?
TF-IDF (Term Frequency–Inverse Document Frequency) measures how important a word is in a document relative to others.
Working:
1. Convert all FAQ questions into TF-IDF vectors
2. Convert user query into TF-IDF vector
3. Compute cosine similarity
4. Select the most similar question
5. Return corresponding answer
Why TF-IDF?
• Handles partial matches
• Works well for text similarity
• Better than direct string matching
Example:
User Query: Tell me about hostel
Matched FAQ: What are hostel facilities?
Answer Returned: Separate hostels are available for boys and girls.
 
🔹 TASK 5: INTENT CLASSIFICATION FOR QUERIES
Explanation:
Intent classification identifies what the user wants.
Defined Intents:
• Admission
• Fees
• Hostel
• Exam
• Contact
Machine Learning Model Used:
• TF-IDF Vectorizer
• Multinomial Naive Bayes Classifier
Training Process:
1. Sample sentences created for each intent
2. Text is preprocessed
3. TF-IDF features extracted
4. Naive Bayes model trained
Example:
Query: How much is the college fee?
Predicted Intent: fees
 
🔹 TASK 6: PIPELINE IMPLEMENTATION
What is a Pipeline?
A pipeline combines multiple steps into a single workflow.
Pipeline Components:
1. TF-IDF Vectorizer → Feature Extraction
2. Multinomial Naive Bayes → Classification
Advantages:
• Clean code
• Less error-prone
• Easy to train and predict
 
🔹 TASK 7: FINAL CHATBOT INTEGRATION
Working:
1. User enters query
2. Query is preprocessed
3. Intent is predicted
4. Correct FAQ answer is returned
5. Chat continues until user exits
Result:
The chatbot provides:
• Fast responses
• Accurate intent detection
• Automated query handling
 
5. RESULTS AND OUTPUT
• Chatbot successfully answers student queries
• Handles different wordings
• Classifies queries accurately
• Reduces manual workload
 
6. APPLICATIONS
• College websites
• Student help desks
• Admission portals
• Educational institutions
 
7. LIMITATIONS
• Limited dataset
• No voice support
• Requires predefined intents
 
8. FUTURE ENHANCEMENTS
• Deep learning models
• Voice-based chatbot
• Multilingual support
• Web-based deployment
 
9. CONCLUSION
This project demonstrates the effective use of NLP and Machine Learning to build a student FAQ chatbot. The system automates query handling and improves efficiency. With further enhancements, it can be deployed in real-world educational environments.
 
