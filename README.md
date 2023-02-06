# My-NLP
Assignment are in homework




| Title | Time Traveler: Reinforcement Learning for Temporal Knowledge Graph Forecasting (EMNLP,2021) |
|----------------|-----------|
| Problems | They do TKG (Temporal knowledge graph) extrapolation to predict the future. For example, "Who is going to be the Thailand Prime Minister in 2023?". <br> The challenge of this work is:<br> 1. Unseen timestamp <br> 2. Unseen entities (subject or object) |
| Key Related Work | 1. Static Knowledge Graph Reasoning <br>2. Temporal Knowledge Graph Reasoning |
| Solution | They designed a Reinforcement learning framework and policy network and made the agent named TITer travel on the TKG to find the answer.<br>For unseen entities, they represented them by leveraging the query information and embeddings of the trained entities, named Inductive Mean (IM). |
| Results  | - They used 4 public TKG datasets (ICEWS14, ICEWS18, WIKI, YAGO) and split data for train, validate, and test by timestamps (used old time to train and test with newer time). <br>- They compared with other TKG models using Mean Reciprocal Rank and performance matrix Hits@1/3/10.<br>- The result showed that TITer (their model) outperformed all other models (TTransE, TA-DistMult, DE-SimplE, RE-NET, xERTE, etc.) in every dataset except ICEWS18 which had the least proportion of unseen entities. |




| Topic | A Fast and Accurate Dependency Parser using Neural Networks |
|----|----|
| Problems | Traditional methods for dependency parsing can be slow and produce inaccurate results |
| Key related work |Transition-based parsing algorithms, Neural network-based approaches |
| Solution | The authors proposed a new model that combines the strengths of both transition-based parsing and neural network-based approaches. The model uses a neural network to make parsing decisions, but relies on a transition-based algorithm to maintain efficiency and handle complex cases |
| Result | The authors showed that their model achieved fast and accurate parsing results, with improved performance compared to existing methods. The model was also shown to be scalable, making it suitable for real-world applications. |


|Topic| Self-Supervised Curriculum Learning for Spelling Error Correction (EMNLP,2021)|
|----|----|
| Problems | the data from different language learners are naturally distributed at different difficulty levels, designing
a curriculum correspondingly for model learning may also help its training and bring about
better performance |
| Key Related Work| 1. Spelling Error Correction (SEC)<br>2. Curriculum Learning (CL)<br>3. Self-Supervised Learning (SSL)|
| Solution | Do Self-Supervised Learning Curriculum Learning (SSCL) which is try to train model by using dataset that have low to high difficulty by <br> 1.check word difficulty<br>2.evaluate model competence<br>3. select data sample that not difficult more than model competence <br> 4. compute data weights (w sample and w token)  |
| Results| compare their method (SSCL) with Uncertainty-Aware CL (UACL) and Norm-Based CL(BACL) <br> by using model Soft-Masked BERT and dataset SIGHAN 2015 Chinese spelling check their model got highest F1-score (74.38) <br> Ablation study <br> 1. use both w data and w token better than use only one <br>lamda (a task-independent hyperparameter to control the
length of the curriculum) proper value is at at 0.9|
