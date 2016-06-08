1: Text Summarization Using Neural Networks  
https://digital.library.txstate.edu/bitstream/handle/10877/3819/fulltext.pdf  

2: A Neural Attention Model for Sentence Summarization  
http://www.aclweb.org/anthology/D15-1044  
  
3: Query-Oriented Multi-Document Summarization via Unsupervised Deep Learning  
http://www.aaai.org/ocs/index.php/AAAI/AAAI12/paper/view/5058  

Paper 3 involves 3 steps:  
1.Concept Extraction :  Create feature vectors which has the tf values of the words in the vocabulary, filter words appearing accidentally at Layer 1, discover key words at Layer 2.  
  
2.Reconstruction Validation : Backpropogate to obtain optimal parameters  
  
3.Summary Generation  :  Constuct an importance-matrix , and extract ten words with max importance scores. Calcluate the importance of sentence by using the union of extracted words.  
  
For the Hidden Layer, Restricted Boltzmann Machines(RBMs) are used  

4: Abstractive Sentence Summarization with Attentive Recurrent Neural Networks  
http://nlp.seas.harvard.edu/papers/naacl16_summary.pdf  

5: Ranking with Recursive Neural Networks and Its Application to Multi-DocumentSummarization  
http://dl.acm.org/citation.cfm?id=2886620  

(Still looking for other 5 relevant papers)  



