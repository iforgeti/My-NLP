# My-NLP
Assignment are in homework


|Title | Time Traveler: Reinforcement Learning for Temporal Knowledge Graph Forecasting|
|----------------------------------|------------------------------|
|Problems | They do the TKG (Temporal knowledge graph) extrapolation type to predict future. For example, “Who going to be Thailand Prime Minister in 2023?”.  
The challenge of this work is.
 1. Unseen timestamp 
 2. Unseen entities (subject or object)
|
|Key Related Work | 1. Static Knowledge Graph Reasoning
2. Temporal Knowledge Graph Reasoning
|
|Solution | They design Reinforcement learning framework and policy network and make the agent named TITer travel on the TKG to find answer.
 For unseen entities they represent unseen entities by leveraging the query information and embeddings of the trained entities, named Inductive Mean (IM)
|
|Results | They use 4 public TKG dataset that ICEWS14, ICEWS18, WIKI,YAGO and split data for train validate and test by timestamps. (Used old time to train and test with newer time)
they compare with other TKG model with Mean Reciprocal Rank and performance matrix Hits@1/3/10
the result is TITer (their model) outperform all other model (TTransE, TA-DistMult, DE-SimplE, RE-NET, xERTE  etc.) in every dataset except ICEWS18 which has least unseen entities proportion.
|
