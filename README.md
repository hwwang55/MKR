# MKR

This repository is the implementation of MKR.


### Files in the folder

- `data/`
  - `book/`
    - `BX-Book-Ratings.csv`: raw rating file of Book-Crossing dataset;
    - `item_index2entity_id.txt`: the mapping from item indices in the raw rating file to entity IDs in the KG;
    - `kg.txt`: knowledge graph file;
  - `movie/`
    - `item_index2entity_id.txt`: the mapping from item indices in the raw rating file to entity IDs in the KG;
    - `kg.txt`: knowledge graph file;
    - `ratrings.dat`: raw rating file of MovieLens-1M;
  - `music/`
    - `item_index2entity_id.txt`: the mapping from item indices in the raw rating file to entity IDs in the KG;
    - `kg.txt`: knowledge graph file;
    - `user_artists.dat`: raw rating file of Last.FM;
- `src/`: implementations of RippleNet.




### Running the code
- Movie
  - ```
    $ cd src
    $ python preprocess.py --dataset movie
    $ python main.py
    ```
- Book
  - ```
    $ cd src
    $ python preprocess.py --dataset book
    ```
  - open `main.py` file;
    
  - comment the code blocks of parameter settings for MovieLens-1M;
    
  - uncomment the code blocks of parameter settings for Book-Crossing;
    
  - ```
    $ python main.py
    ```
- Music
  - ```
    $ cd src
    $ python preprocess.py --dataset music
    ```
  - open `main.py` file;
    
  - comment the code blocks of parameter settings for MovieLens-1M;
    
  - uncomment the code blocks of parameter settings for Last.FM;
    
  - ```
    $ python main.py
    ```