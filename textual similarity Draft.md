__Mögliche Datensets__:
-
Hugging Face -- stsb_multi_mt_dataset

__Preprocessing der Daten__:
-
  - Split in trainings und testdaten
  - Lemmatisierung, entfernen von Zahlen und Funktionswörtern --> Praktisch mit spacy en_core_web_sm
  - Tokenisieren der Sätze

__Vergleich von Ähnlichkeits-Metriken__:
-
  - Cosinusähnlichkeit --> sklearn cosine_similarity
  - Jaccard-Ähnlichkeit --> Vergleich der Unique-words in zwei Sätzen mit text_distance_library
  - W-shingling von Jaccard-Ähnlichkeit --> Ähnlichkeit zwischen verschiedenen Längen von N-grams statt nur Unigramme zu verwenden.
  - Bag of Words --> Ähnlichkeit zwischen Embedding-Vektoren mit Cosinus-Ähnlichkeit
  - Word Movers Distance (WMD) --> geht nicht davon aus, dass ähnliche Texte auch ähnliche Worte enthalten.
 
 ### Bag of Words ###
  1. Count Vectorizer --> mappt jedes unique Wort im gesamten Text-Korpus auf einen uniquen Vekor-Index. Die Vektor-Werte für jedes Dokument/Satz sind die Anzahl der Vorkommnisse jedes spezifischen Wortes im Text.
  Alle Wörter werden gleich behandelt, egal, ob die Wörter wirklich wichtig sind oder nicht!!!
  2. TFIDF Vectorizer --> Benutzt gleiche Methode wie der Count Vectorizer, aber die Werte sind nun Produkt von Term-Frequency und Inverse-Document-Frequency. Berücksichtigt wie wichtig einzelne Worte für ein bestimmtes Dokument sind.
  3. Für beides kann die sklearn Library zur feature extraction benutzt werden. TFIDF muss aber trainiert werden, um die unique-words des gesamten Korpus lernen.
  4. Model = TfifdVectorizer
 
 ### Word Movers Distance ###
  1. Benutzt pre-trained word-embeddings mit Word2Vec, GloVe, FastText, etc.
  2. WMD --> minimale Distanz zwischen den Word-Embeddings des einen Satzes, die "überbrückt" werden muss, um die Word-Embeddings des zu vergleichenden Satzes zu "
 erreichen". Wird für jedes Wort des Satzes berechnet.
  3. Der "überbrückte" Abstand wird mit den Term-Frequencies jedes Wortes gewichtet.
  4. Kann mit der gensim library und dem Fast WMD Algorithm berechnet werden.
  5. Die pre-trained Modelle können verglichen werden. Aber FastText ist vermutlich am besten, da dieses auf Wikipedia trainiert ist und am wenigsten Wahrscheinlich den Error "Out of Vocabulary" anzeigt, anders als bei Word2Vec oder Glove.
  6. Metrik ist DISTANZ! Also mit -1 multiplizieren, damit größere Abstände schlechter sind.

__Vergleich mit Modern contextual algorithms__:
-
  - Universal sentence Encoder (USE) --> Tranformer Model mit tensorflow
  - Cross Encoder --> BERT, RoBERTa, etc.
  - Metric Learning
  - SBERT Bi-Encoder
  - SimCSE
  - OpenAI (maybe)
