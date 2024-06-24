Data Preparation
Folder Structure:

Extracted Articles: Contains text files extracted from articles.
Stopwords and Master Dictionary:

StopWords: Contains multiple text files with stopwords categorized into different domains.
MasterDictionary: Contains text files with positive and negative words.
2. Text Preprocessing
Cleaning Text:

Removing Stopwords: Load stopwords from the StopWords folder to exclude them from the text.
Removing Punctuation: Clean text by removing punctuation marks like ?, !, ,, ..
Tokenization:

NLTK Tokenization: Convert cleaned text into tokens (words) using NLTK's word_tokenize.
3. Sentiment Analysis
Positive and Negative Words:

Loading Positive and Negative Words: Load positive and negative words from the MasterDictionary folder excluding stopwords.
Scoring:

Positive Score: Assign +1 for each positive word found in the text.
Negative Score: Assign -1 for each negative word found in the text (multiplied by -1).
Polarity Score: Calculate using the formula: (Positive Score - Negative Score) / ((Positive Score + Negative Score) + 0.000001).
Subjectivity Score: Calculate using the formula: (Positive Score + Negative Score) / (Total Words after cleaning + 0.000001).
4. Readability Analysis
Metrics Calculation:

Average Sentence Length: Number of words divided by the number of sentences.
Percentage of Complex Words: Number of complex words divided by the total number of words.
Fog Index: Calculate using the formula: 0.4 * (Average Sentence Length + Percentage of Complex Words).
5. Additional Text Metrics
Average Number of Words per Sentence:

Calculate as Total number of words / Total number of sentences.
Complex Word Count:

Count words with more than two syllables.
Syllable Count per Word:

Count syllables in each word considering special cases like words ending with "es", "ed".
Personal Pronouns:

Count occurrences of specific personal pronouns using regex, excluding exceptions like "US".
Average Word Length:

Calculate as Sum of the total number of characters in each word / Total number of words.
6. Data Output
Excel File Generation:

Store all calculated metrics for each article in an Excel file.



7. Tools and Libraries
Python: Programming language used for scripting.
NLTK (Natural Language Toolkit): Library for natural language processing tasks such as tokenization and stopwords removal.
Pandas: Library for data manipulation and analysis, used for creating and writing to Excel files.
Regular Expressions (Regex): Used for pattern matching, particularly for identifying personal pronouns.
