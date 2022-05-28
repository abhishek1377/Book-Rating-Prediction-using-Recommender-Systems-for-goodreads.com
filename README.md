# Book-Rating-Prediction-using-Recommender-Systems-for-goodreads.com

We have created various models to predict prospective user ratings for unread books for goodreads.com in Poetry genre. We Used methods such as item-item CF, Matrix factorization with neural CF, and Neural Matrix factorization to build models. We have achieved MAE of 0.779 and MSE of 0.964 signifying our predictions to be within error margin of 1 for a 0-5 rating system. Model results can be used to provide recommendations to users based on highest prospective rating as well as the next item prediction recommendation.


1.	Data extraction
  •	Data Download: Goodreads poetry dataset (https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home)
  
  
    •	Poetry dataset download link(https://drive.google.com/uc?id=17G5_MeSWuhYnD4fGJMvKRSOlBqCCimxJ)
      i.	Downloads goodreads_interactions_poetry.json.gz 

    •	Book genres data download link(https://drive.google.com/uc?id=1ah0_KpUterVi-AHxJ03iKD6O0NfbK0md)
      i.	Downloads gooreads_book_genres_initial.json.gz

    •	User_id map download link(https://drive.google.com/uc?id=15ax-h0Oi_Oyee8gY_aAQN6odoijmiz6Q)
      i.	Downloads user_id_map.csv

    •	Book_id map download link(https://drive.google.com/uc?id=1CHTAaNwyzvbi1TR08MJrJ03BxA266Yxr)
      i.	Downloads book_id_map.csv

  •	Data Preprocessing: 
    •	Notebook used – preprocessing.ipynb 

      i.	Generates the following files 
        •	interactions.csv
        •	Interactions_full.csv
        •	Interactions_genres.csv
        •	user matrix factorized embeddings - ‘user.pickle’
        •	Book matrix factorized embeddings - ‘book.pickle’

2. Item-Item CF
  •	Datasets:
    I.	goodreads_books_poetry.json.gz
    II.	goodreads_reviews_poetry.json.gz
    III.	user_id_map.csv
    IV.	book_id_map.csv

  •	Notebooks: 
    I.	Item_Item_Collaborative_Filtering_for_Goodreads.ipynb

  •	Instructions: 
    I.	Run Item_Item_Collaborative_Filtering_for_Goodreads.ipynb file to load the json.gz files
    II.	Run the rest of the notebook to generate item-item collaborative filtering results and evaluation metrics.

3.  NCF with MF:
  •	Datasets: 
    I.	goodreads_interactions_poetry.json.gz
    II.	user_id_map.csv
    III.	book_id_map.csv

  •	Notebooks: 
    I.	embeddings.ipynb
    II.	ncf_mf.ipynb

  •	Instructions:
    I.	run embeddings.ipynb to create user_item_ratings.csv, reader and book embeddings.
    II.	run ncf_mf.ipynb to build model and generate results.

4. NeuMF:
  •	Datasets:
    I.	interactions.csv

  •	Notebooks: 
    I.	NeuMf.ipynb

  •	Instructions:
    I.	Run NeuMf.ipynb to build model and generate results for Neural Matrix Factorization model.

5. NeuMF with Genres:
  •	Datasets:
    I.	interactions_genres.csv

  •	Notebooks:
    II.	neumf_with_genres.ipynb

  •	Instructions: 
    III.	Run neumf_with_genres.ipynb to build model and generate results for Neural Matrix Factorization with genres model

