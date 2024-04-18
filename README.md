### Quantitative Analysis of Semantic Shift
In a diachronic perspective, examine how the semantic shift of a word affects its corresponding word embeddings and analyse the contexts in which these shifts occur. 

Corpora used for the diachronic analysis:
COHA: Corpus of Historical American English, a sample of 8.9 million words. US, 1810-2009
COCA: Corpus of Contemporary American English, a sample of 3.6 million words. US, 1990-2019

We contrast quantitatively the vector representations of 20 words.
10 words that didn’t undergo a semantic change within XIX-XXI centuries (they did change their meaning but in earlier centuries): 
accident, business, disease, face, girl, governor, nice, pudding, thing, wife
10 words that are known to significantly change their meaning between the two given periods:  broadcast, bug, cool, gay, post, queer, silly, terrific, virus, web

METHOD
We replicate the methodology of previous studies (Hamilton et al., 2016a and 2016b) that examined a similar topic with some minor revisions. In our work, instead of performing the diachronic analysis over a series of decades, we perform the analysis with an aggregate spanning two different centuries: 1810 to 1910 against 1990 to 2019. This was done because while trying the diachronic analysis by decade, several of our target words did not occur frequently enough for the model to capture. So, to increase the word frequency, we perform the analysis over a broader period.

Method for evaluation and analysis: 
Once the word embeddings were created, the initial step was to compare them between the two corpora by replicating the measures developed by Hamilton et al. (2016a):
Global Measure (GM) is the cosine distance between a given word s vectors from two periods. The greater distance corresponds to a more significant semantic change (Kim et al., 2014; Dubossarsky et al., 2017); 
Local Neighbourhood Measure (LNM) evaluates the semantic shift based on the degree of change of its corresponding semantic neighbours between two periods.
