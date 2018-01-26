# Food2Vec
An exploration into the world of fusion recipes and creative cooking with NLP. 

Food2vec uses a combination of natural language processing and supervised and unsupervised learning to create cuisine profiles based on a large collection of recipes with ingredient lists and instructions. The cuisine profiles can be applied like filters to existing recipes to generate new recipes where the original meal has been transformed in the style of the desired cuisine.

**Data:**
Dataset from a [Kaggle competition](https://www.kaggle.com/hugodarwood/epirecipes); originally 
from Epicurious.com.

**Tools:**
* Data Storage: MongoDB
* Natural Language Processing: gensim/word2vec, NLTK, Ingreedy
* Supervised Learning: classification algorithms
* Dimensionality Reduction/PCA

**Files:**
* 01_data_load.ipynb: Upload/pull Epicurious data from MongoDB and create initial dataframe
* 02_cbow_process.ipynb: Turn all text data into continuous bags of words
* 03_word2vec.ipynb: Convert CBOWs into document vectors
* 04_cuisine_tags.ipynb: Label recipes by cuisines; label unlabeled recipes with ensemble classification model 
* 05_cuisine_profiles.ipynb: Create cuisine profiles by calculating the probability of each ingredient to appear in each cuisine 
* 06_custom_word2vec.ipynb: Use recipe data to train a custom word2vec model
* 07_custom_doc2vec.ipynb: Convert CBOWs into document vectors with custom word2vec model
* 08_food_clusters.ipynb: Unsupervised clustering to determine groups of ingredients
* 09_ingredient_parser_recipe_generator.ipynb: Identify replaceable ingredients in a recipe and substitute them with ingredients most likely to appear in the desired cuisine.
* food2vec_deck.pdf: Presentation; video of the presentation available [here](https://livestream.com/metis/events/7832294) from time 15:24 to 22:31

