<b>1: Text Summarization Using Neural Networks  </b>  
https://digital.library.txstate.edu/bitstream/handle/10877/3819/fulltext.pdf  

In short, build feature vector using info such as tf,idf for every sentence in a document using and feed it to a neural net.  
As discussed, this approach is very trivial ,hence not working on this paper. 

<b>2: Text Summarization using Neural Networks and Rhetorical Structure Theory </b>  
http://www.ijarcce.com/upload/2015/june-15/IJARCCE%2012.pdf  

This paper is almost the same as the first paper.  

<b>3: Ranking with Recursive Neural Networks and Its Application to Multi-document Summarization:  </b>  

Since feature engineering is laborous,it's better to let the model discover
explanatory factors from data. RNN learns ranking features automatically.
It sort of supplements the hand-crafted features with learned features.
To build the hand-crafted feature matrix,build a parse tree of every sentence using stanford coreNLP and 
use this information in the feature matrix.

<b>4: Query-Oriented Multi-Document Summarization via Unsupervised Deep Learning  </b>  
http://www.aaai.org/ocs/index.php/AAAI/AAAI12/paper/view/5058  

Paper 3 involves 3 steps:  
1.Concept Extraction :  Create feature vectors which has the tf values of the words in the vocabulary, filter words appearing accidentally at Layer 1, discover key words at Layer 2.  
  
2.Reconstruction Validation : Backpropogate to obtain optimal parameters  
  
3.Summary Generation  :  Constuct an importance-matrix , and extract ten words with max importance scores. Calcluate the importance of sentence by using the union of extracted words.  
  
For the Hidden Layer, Restricted Boltzmann Machines(RBMs) are used  

<b>4: Reader-Aware Multi-Document Summarization via Sparse Coding∗  </b>

I think this paper doesn't involves deep learning.  





