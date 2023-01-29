# My-NLP
Assignment are in homework




Title	Time Traveler: Reinforcement Learning for Temporal Knowledge Graph Forecasting
Problems	- They do TKG (Temporal knowledge graph) extrapolation to predict the future. For example, "Who is going to be the Thailand Prime Minister in 2023?"<br>- The challenge of this work is:<br>    1. Unseen timestamp<br>    2. Unseen entities (subject or object)
Key Related Work	1. Static Knowledge Graph Reasoning<br>2. Temporal Knowledge Graph Reasoning
Solution	- They designed a Reinforcement learning framework and policy network and made the agent named TITer travel on the TKG to find the answer.<br>- For unseen entities, they represented them by leveraging the query information and embeddings of the trained entities, named Inductive Mean (IM).
Results	- They used 4 public TKG datasets (ICEWS14, ICEWS18, WIKI, YAGO) and split data for train, validate, and test by timestamps (used old time to train and test with newer time).<br>- They compared with other TKG models using Mean Reciprocal Rank and performance matrix Hits@1/3/10.<br>- The result showed that TITer (their model) outperformed all other models (TTransE, TA-DistMult, DE-SimplE, RE-NET, xERTE, etc.) in every dataset except ICEWS18 which had the least proportion of unseen entities.
