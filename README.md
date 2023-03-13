# My-NLP
Assignment are in homework

## parse paper

| Topic | A Fast and Accurate Dependency Parser using Neural Networks |
|----|----|
| Problems | Traditional methods for dependency parsing can be slow and produce inaccurate results |
| Key related work |Transition-based parsing algorithms, Neural network-based approaches |
| Solution | The authors proposed a new model that combines the strengths of both transition-based parsing and neural network-based approaches. The model uses a neural network to make parsing decisions, but relies on a transition-based algorithm to maintain efficiency and handle complex cases |
| Result | The authors showed that their model achieved fast and accurate parsing results, with improved performance compared to existing methods. The model was also shown to be scalable, making it suitable for real-world applications. |

---

## paper 1

| Title | Time Traveler: Reinforcement Learning for Temporal Knowledge Graph Forecasting (EMNLP,2021) |
|----------------|-----------|
| Problems | They do TKG (Temporal knowledge graph) extrapolation to predict the future. For example, "Who is going to be the Thailand Prime Minister in 2023?". <br> The challenge of this work is:<br> 1. Unseen timestamp <br> 2. Unseen entities (subject or object) |
| Key Related Work | 1. Static Knowledge Graph Reasoning <br>2. Temporal Knowledge Graph Reasoning |
| Solution | They designed a Reinforcement learning framework and policy network and made the agent named TITer travel on the TKG to find the answer.<br>For unseen entities, they represented them by leveraging the query information and embeddings of the trained entities, named Inductive Mean (IM). |
| Results  | - They used 4 public TKG datasets (ICEWS14, ICEWS18, WIKI, YAGO) and split data for train, validate, and test by timestamps (used old time to train and test with newer time). <br>- They compared with other TKG models using Mean Reciprocal Rank and performance matrix Hits@1/3/10.<br>- The result showed that TITer (their model) outperformed all other models (TTransE, TA-DistMult, DE-SimplE, RE-NET, xERTE, etc.) in every dataset except ICEWS18 which had the least proportion of unseen entities. |

## paper 2

|Topic| Self-Supervised Curriculum Learning for Spelling Error Correction (EMNLP,2021)|
|----|----|
| Problems | -the data from different language learners are naturally distributed at different difficulty levels  <br> -they expect designing a curriculum correspondingly for model learning may help SEC training and bring about better performance |
| Key Related Work| 1. Spelling Error Correction (SEC)<br>2. Curriculum Learning (CL)<br>3. Self-Supervised Learning (SSL)|
| Solution | Do Self-Supervised Learning Curriculum Learning (SSCL) which is try to train model by using dataset that have low to high difficulty by <br> 1.check word  difficulty<br>2.evaluate model competence<br>3. select data sample that not difficult more than model competence <br> 4. compute data weights (w sample and w token)  |
| Results| -test <br> compare their method (SSCL) with Uncertainty-Aware CL (UACL) and Norm-Based CL(BACL) <br> by using model Soft-Masked BERT and dataset SIGHAN 2015 Chinese spelling check their model got highest F1-score (74.38) <br> -Ablation study <br> 1. use both w data and w token better than use only one <br> 2.lamda (a task-independent hyperparameter to control the length of the curriculum) proper value is at at 0.9|

## paper 3

|Topic| COCO-LM: Correcting and Contrasting Text Sequences for Language Model Pretraining (NIPS,2021) |
|----|----|
| Problems| they found pretrain self-supervised learning have main 2 challenge <br> 1. after a certain point, model that used for pretraining by standard token-level language modeling stop improve <br> 2. pre-trained language models might not capture the relationships between different elements of the input text |
| Key Related Work |  1. Various token-level tasks <br> 2. Sequence-level tasks <br> 3. MLM <br> 4. ELECTRA <br> 5. contrastive learning  |
| Solution | they present COCO-LM which is combine technique of both MLM and ELECTRA pretraining. In brif, they use generator tranfromer to predict missing token and feed that predict to discraminator,but they use CLM instead of binary classification score and they use SCL to contrast the corrupted sequences with crop sequences |
| Results | The COCO-LM objective outperforms other state-of-the-art pre-training objectives on several language tasks, including text classification, natural language inference, and question answering. The authors also show that fine-tuning a model pre-trained with COCO-LM on downstream tasks leads to further improvements in performance.   |

## paper 4

|Topic| Exploiting Cloze Questions for Few Shot Text Classification and Natural Language Inference (EMNLP, 2021) |
|----|----|
| Problems | Prompt base learning is underperforms supervised learning |
| Key Related Work | 1. Few-shot learning <br> 2. Cloze-style question answering |
| Solution | Combined supervised with few shot setting by reformulate input examples into cloze-style phrases <br>the method is call Pattern-Exploiting Training --> train masked languages model by give input, pattern and map between label. make model to answer label base on pattern.|
| Result | evaluate their method on many benchmark datasets, and show that it outperforms several state-of-the-art few-shot learning methods and supervised and unsupervised methode especially on small dataset.
