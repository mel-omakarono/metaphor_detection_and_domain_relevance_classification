# metaphor_detection_and_domain_relevance_classification
Metaphor Detection and Domain Relevance Classification in Immunotherapy Texts


This repository belongs to the Master's Thesis Project "Staying Relevant: Metaphor Detection and Domain Relevance Classification in Immunotherapy Texts" by Melina Paxinou, supervised by Dr. Pia Sommerauer and Gudrun Reijnierse. 

The purpose of this thesis is to evaluate whether models trained for metaphor detection can be outperformed by models with domain-specific pre-training, with a particular focus on the field of immunotherapy. The first task, Metaphor Detection, is a binary classification problem at a token level, where the goal is to predict whether a given metaphorical token is related to immunotherapy, using both a general-domain and a domain-adapted RoBERTa model. The second task, Domain Relevance Classification, focuses on identifying metaphors directly related to the domain of immunotherapy using a BERT model. Both tasks use data derived from the Vrije Universiteit Amsterdam (VUA) Metaphor Corpus and the Immunotherapy Metaphor Dataset compiled by Bos et al. (2025) from scientific publications and news articles. This setup provides a concrete test of whether the knowledge captured from biomedical texts during pre-training improves metaphor detection in a specialized domain. 

The results show that while BioMed-RoBERTa is more sensitive to metaphorical language, its increased detection comes with greater noise, which reduces relevance precision. In contrast, XLM-RoBERTa paired with the BERT classifier achieves better overall pipeline performance. This work shows the promise of current metaphor detection approaches for science communication and reveals their weaknesses. 

By improving metaphor detection and domain relevance classification, the proposed pipeline aims to support automated analyses of how metaphor shapes science communication, with implications for public understanding and expert discourse around complex scientific concepts.


## Project Structure

<pre>
project-root
├── domain_relevance
│   ├── baseline.ipynb
│   └── metaphor_bert.ipynb
├── metaphor_detection
│   └── biomed_metaphor_detection.ipynb
├── preprocessing
│   └── datasets.ipynb
├── LICENSE
├── Melina_Paxinou_thesis.pdf
├── README.md
├── full_pipeline_metaphor_relevance.ipynb
└── requirements.txt
</pre>



`baseline.ipynb` This file contains the code for the creation of the Logistic Regression model used as a baseline for the Domain Relevance Classification task. 

`metaphor_bert.ipynb` This file contains the code for the creation of the BERT model used for the Domain Relevance Classification task. The code used to fine-tune the BERT model was adapted from materials provided in the Machine Learning for NLP course, part of the Text Mining specialization within the Linguistics Master at Vrije Universiteit Amsterdam.

`biomed_metaphor_detection.ipynb` This file contains code derived from https://github.com/lwachowiak/Multilingual-Metaphor-Detection/tree/main, which was used to train BioMed-RoBERTa for the task of Metaphor Detection. 

`datasets.ipynb` This file contains snippets of code used to modify and adapt the original version of the Immunotherapy Metaphor Dataset into the forms used to train and test the models of this thesis. 

`full_pipeline_metaphor_relevance.ipynb` This file contains the code used to run the full pipeline on the Annotated Immunotherapy Subset, from metaphor detection to domain relevance classification. 

`Melina_Paxinou_thesis.pdf` The pdf file contains the full thesis report.

The data used in this thesis is not allowed to be shared due to confidentiality reasons. 
