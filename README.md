# NER-Crowd-Annotation

## Annotation Settings

In Dialog domain (DL), we collect raw sentences from a chatbot application. And then we randomly select 20K sentences as our pool and hire 43 students to annotate the sentences. 

We ask the annotators to label two types of entities: Person-Name and Song-Name. The annotators label the sentences independently. In particular, each sentence is assigned to three annotators for this data.

Finally, we have 16,948 sentences annotated by the students. The average length of all sentences is 9.21. The average Kappa value among the annotators is 0.6033

## Data Format

Concretely, we randomly select 1,000 sentences from the final dataset and let two experts generate the gold annotations. Among them, we use 300 sentences as the development set and the remaining 700 as the test set. The rest sentences with only student annotations are used as the training set.

Final dataset should be in the following format, divided into four columns:

```
嗯	oth	O	1427402039
,	pun	O	1427402039
听	oth	O	1427402039
一	oth	O	1427402039
首	oth	O	1427402039
雨	oth	B	1427402039
花	oth	I	1427402039
石	oth	E	1427402039
。	pun	O	1427402039
```

In particular, the last column is user_id of annotator.

## Pre-trained Embeddings

The pre-trained embeddings are trained by tool word2vec on 5M sentences which are the user-generated text from Internet. We set the embedding dimension as 100, the minimum frequency of occurrence as 5, and the window size of 5. The embeddings file is available at .\DL-PS\pre-trained.emb.

## Cite

If you use the data, please cite the following paper:

[Yang et al., 2018] YaoSheng Yang, Meishan Zhang, Wenliang Chen, Haofen Wang, Wei Zhang, Min Zhang. Adversarial Learning for Chinese NER from Crowd Annotations, Proceedings of AAAI-2018, pp1627-1634, New Orleans, USA,Feb 2018[C]