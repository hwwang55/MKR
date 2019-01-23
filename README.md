# MKR

This repository is the implementation of MKR (arXiv link is coming soon):

> Multi-Task Feature Learning for Knowledge Graph Enhanced Recommendation  
Hongwei Wang, Fuzheng Zhang, Miao Zhao, Wenjie Li, Xing Xie, and Minyi Guo.  
In Proceedings of The 2019 Web Conference (WWW 2019)

![](https://github.com/hwwang55/MKR/blob/master/framework.png)

MKR is a **M**ulti-task learning approach for **K**nowledge graph enhanced **R**ecommendation.
MKR consists of two parts: the recommender system (RS) module and the knowledge graph embedding (KGE) module. 
The two modules are bridged by *cross&compress* units, which can automatically learn high-order interactions of item and entity features and transfer knowledge between the two tasks.


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
- `src/`: implementations of MKR.




### Running the code
- Movie
  ```
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