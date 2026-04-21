

## **Aim**

To study and implement basic **Natural Language Processing (NLP)** techniques in Python using the NLTK library, including tokenization, stopword removal, stemming, lemmatization, part-of-speech tagging, and frequency distribution analysis of text data.

---

## **Theory**

**Natural Language Processing (NLP)** is a subfield of Artificial Intelligence that focuses on enabling computers to understand, interpret, and process human language. It is widely used in applications like chatbots, sentiment analysis, translation, and search engines.

In this experiment, various NLP preprocessing techniques are implemented using Python libraries.

### **1. Tokenization**

Tokenization is the process of breaking text into smaller units like words or sentences.

* **Function:** `word_tokenize(text)`

  * **Use:** Splits a sentence into individual words (tokens).
  * Example: `"NLP is fun"` → `['NLP', 'is', 'fun']`

* **Function:** `sent_tokenize(text)`

  * **Use:** Splits a paragraph into sentences.
  * Example: `"Hello. How are you?"` → `['Hello.', 'How are you?']`

---

### **2. Stopwords Removal**

Stopwords are commonly used words (like “is”, “the”, “and”) that do not carry significant meaning.

* **Function:** `stopwords.words('english')`

  * **Use:** Returns a list of common English stopwords.

* **Process Used:**

  ```python
  [w for w in words if w.lower() not in stop_words]
  ```

  * **Use:** Removes stopwords from the tokenized words to retain meaningful data.

---

### **3. Stemming**

Stemming reduces words to their root form, often by removing suffixes.

* **Class:** `PorterStemmer()`

  * **Use:** Applies Porter stemming algorithm.

* **Function:** `stemmer.stem(word)`

  * **Use:** Converts words to base/root form.
  * Example: `"running"` → `"run"`

---

### **4. Lemmatization**

Lemmatization converts words to their meaningful base form (lemma) using vocabulary and grammar.

* **Class:** `WordNetLemmatizer()`

  * **Use:** Provides more accurate root words compared to stemming.

* **Function:** `lemmatizer.lemmatize(word)`

  * **Use:** Returns the dictionary form of a word.
  * Example: `"studies"` → `"study"`

---

### **5. Part-of-Speech (POS) Tagging**

POS tagging assigns grammatical labels to words like noun, verb, adjective, etc.

* **Function:** `pos_tag(words)`

  * **Use:** Tags each word with its grammatical category.
  * Example: `"python is powerful"` → `[('python', NN), ('is', VBZ), ('powerful', JJ)]`

---

### **6. Frequency Distribution**

Frequency distribution counts how often each word appears in a text.

* **Class:** `FreqDist(words)`

  * **Use:** Creates a frequency distribution object.

* **Function:** `fd.most_common()`

  * **Use:** Returns words along with their frequency in descending order.

---

### **7. Data Download Functions**

* **Function:** `nltk.download('punkt')`

  * **Use:** Downloads tokenizer models.

* **Function:** `nltk.download('stopwords')`

  * **Use:** Downloads stopword dataset.

* **Function:** `nltk.download('wordnet')`

  * **Use:** Required for lemmatization.

* **Function:** `nltk.download('averaged_perceptron_tagger')`

  * **Use:** Required for POS tagging.

---

## **Conclusion**

In this experiment, various NLP preprocessing techniques were successfully implemented using Python and the NLTK library. The study demonstrated how raw text can be transformed into structured and meaningful data through tokenization, stopword removal, stemming, and lemmatization. Additionally, part-of-speech tagging and frequency distribution helped in analyzing grammatical structure and word importance.

These techniques form the foundation of advanced NLP tasks such as text classification, sentiment analysis, and machine learning applications. Overall, the experiment provided practical understanding of how textual data is processed and prepared for further analysis in real-world applications.

---

