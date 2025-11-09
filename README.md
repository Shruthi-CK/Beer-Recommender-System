# Beer-Recommender-System

### Project Goal Summary (under 300 words)

This project builds and evaluates a beer recommendation system using 10,000 scraped reviews from BeerAdvocate. The goal is to recommend beers that match a user's specific attribute preferences (e.g., "sweet," "smooth," "hoppy") and have high review sentiment.

The project compares three different NLP models:

1.  **Task B (TF-IDF):** A traditional keyword-matching model that uses a Bag-of-Words approach.
2.  **Task C (SpaCy):** A semantic model using pre-trained general-purpose embeddings (`en_core_web_md`) to understand the meaning of the reviews.
3.  **Task D (Word2Vec):** A custom semantic model trained on the 10,000 beer reviews to capture domain-specific language.

All models work by creating a vector for the user's attributes (expanded with synonyms) and calculating the cosine similarity against vectors for each beer. This similarity score is then combined with a VADER sentiment score for a final ranking.

The analysis concludes that the semantic models (SpaCy and custom Word2Vec) are superior. They successfully recommend a coherent list of beers (e.g., all stouts) based on the flavor profile, while the TF-IDF model gets confused by generic positive words and recommends a mix of unrelated styles.

The project also validates its approach by showing that simply recommending the highest-rated beers (Task E) fails, as it would suggest popular stouts to a user asking for "hoppy" beers.
