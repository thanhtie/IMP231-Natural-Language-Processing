# Natural-Language-Processing

[Explaination](https://www.youtube.com/watch?v=ATK6fm3cYfI): (have a bit changes in tf definition)

---

![image](https://github.com/thanhtie/IMP231-Natural-Language-Processing/assets/92991572/98e7c10d-d644-4312-925a-998783cc8bf1)

![image](https://github.com/thanhtie/IMP231-Natural-Language-Processing/assets/92991572/832fcb9f-6d03-4b74-a04b-ceefb7b420f7)

![image](https://github.com/thanhtie/IMP231-Natural-Language-Processing/assets/92991572/f00acce8-2ff6-44e9-8db2-d61b1d2865ed)


---
### How to calculate:

Step 1: count raw frequency of term in a document

Step 2: calculate the tf by divide raw frequency/(max of frequency in the document)

Step 3: calculate the df for each term

Step 4: calculate the tf-idf by using formula log2(N/df) Note: N is #total of document

Step 5: calculate tf-idf = tf * idf = tf * log2(N/df)

---
### Some real-world applications:

Information Retrieval and Search Engines:

* TF-IDF helps search engines rank documents based on their relevance to a user’s query. It assigns higher weights to terms that appear frequently in a document but are rare across the entire corpus.
* When you search for something on Google, the search results are often ranked using TF-IDF scores.

Document Clustering and Similarity:

* TF-IDF vectors can represent documents as numerical feature vectors. Similar documents will have similar TF-IDF vectors.
* Clustering algorithms (like K-means) use TF-IDF to group similar documents together.
* 
Keyword Extraction:

* By analyzing TF-IDF scores, you can extract important keywords from a document.
* For example, in content summarization, identifying significant terms helps create concise summaries.
  
Content Recommendation Systems:

* TF-IDF assists in recommending relevant articles, blog posts, or products to users.
* It identifies similar content based on shared keywords.
  
Sentiment Analysis and Text Classification:
* In sentiment analysis, TF-IDF features can be used to train machine learning models to classify text as positive, negative, or neutral.
* It’s also useful for topic classification (e.g., categorizing news articles).
  
Extracting Significant Words from Transcripts:
* Imagine analyzing movie or TV show transcripts. TF-IDF can help identify the most significant words and phrases that define the narrative and characters.

---
### Advantages of TF-IDF:
1. Feature Selection:
* TF-IDF helps identify essential terms in a document by assigning higher weights to words that are frequent in the document but rare across the entire corpus.
* This feature selection process enhances the quality of text representations.

2. Dimensionality Reduction:
* By representing documents as TF-IDF vectors, we reduce the dimensionality of the data.
* This is crucial for efficient storage and faster processing in large-scale applications.

3. Language Independence:
* TF-IDF is language-agnostic. It works well across different languages without requiring language-specific preprocessing.
* This makes it versatile for multilingual applications.

4. Document Similarity and Clustering:
* Similar documents have similar TF-IDF vectors, making it useful for clustering and similarity analysis.
* Applications include content recommendation and grouping similar news articles.
  
5. Keyword Extraction:
* TF-IDF helps extract significant keywords from documents.
* Useful for summarization, topic modeling, and content indexing.

### Disadvantages of TF-IDF:
1. Sparse Representations:
* In high-dimensional spaces, most entries in the TF-IDF matrix are zeros.
* Sparse representations can be memory-intensive and affect computational efficiency.

2. Lack of Semantic Understanding:
* TF-IDF treats words as independent features, ignoring their semantic relationships.
* It doesn’t capture context or word meanings.

3. Sensitivity to Document Length:
* Longer documents tend to have higher raw term frequencies.
* Normalization (using sublinear scaling) helps mitigate this, but it’s still a consideration.

4. Overemphasis on Rare Terms:
* Extremely rare terms may receive disproportionately high weights.
* Techniques like smoothed IDF address this issue.
  
5. Stop Words and Common Terms:
* Common words (stop words) often dominate the TF-IDF scores.
* Preprocessing (removing stop words) is necessary to improve results.
