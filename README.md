# Protein sequences embedding using Natural Language Processing (NLP) method
## Summary
Project for pattern recognition exam. The aim is to extract important features which characterize protein sequences of the Spike (S) protein, that is found on the outside of the SARS-CoV-2 virus particle. 
We train a LSTM neural network to classify Spike protein sequences according to their host species in order to get the embedding weights, that is the representation of proteins sequences of
symbols as continuous vectors. Brian Hie et al. in *Learning the language of viral evolution and escape* show that the human sequences are very similar to those
of bat and pangolin sequences. Hence we would like to assess at least these results, even though using an other neural network model. In the end, besides this, we find that human protein sequences arrange themselves in a more
regular shape with respect to animals, which suggests a "more regular and less random" variability in Spike protein sequences from human host species.

A note: this approach uses supervised machine learning model (the neural network has to classify sequences according to their host species) and so this method to represent protein sequences is enriched with prior biological knowledge.
This same concept is widely exploited and examinated in the article *Learning the protein language: Evolution, structure, and function* by Tristan Bepler and Bonnie Berger.

## Dependences
tensorflow, numpy, pandas, matplotlib, collections, scikit-learn. 

## Contents
* [ProteinSequencesNLP_ManuelaCarriero.pdf](https://github.com/ManuelaCarriero/natural-language-processing-project/blob/main/ProteinSequencesNLP_ManuelaCarriero.pdf) has all the theoretical concepts explained which are exploited for the analysis and the relative analysis and discussion.
* [ProteinSequencesNLP_ManuelaCarriero.ipynb](https://github.com/ManuelaCarriero/natural-language-processing-project/blob/main/ProteinSequencesNLP_ManuelaCarriero.ipynb) and [ProteinSequencesNLP_ManuelaCarriero.html](https://github.com/ManuelaCarriero/natural-language-processing-project/blob/main/ProteinSequencesNLP_ManuelaCarriero.html) report the python code used.<br> 
Such first two points considers an approach for the protein sequences embedding based on the average aminoacids (chosen as tokens) embedding obtained from the first layer of the LSTM (the embedding layer).<br> 
In the folder [StandardEmbeddingApproach](https://github.com/ManuelaCarriero/natural-language-processing-project/tree/main/StandardEmbeddingApproach) you can find an other procedure that is commonly used and that exploits the output vector of LSTM layer in Keras.
 
## Data
The protein sequences data analysed ([cov_all.fa](https://github.com/ManuelaCarriero/natural-language-processing-project/blob/main/cov_all.fa)) were available in https://github.com/brianhie/viral-mutation.