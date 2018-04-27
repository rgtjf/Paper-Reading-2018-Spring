# Paper-Reading-2018-Spring

## Previous Edtions

- [Summer_Paper_Reading_2016](https://github.com/rgtjf/Summer_Paper_Reading_2016)
- [Paper-Reading-Third-Edition](https://github.com/rgtjf/Paper-Reading-Third-Edition)
- [Summer_Paper_Reading_2017](https://github.com/rgtjf/Summer_Paper_Reading_2017)

1. Men Also Like Shopping: Reducing Gender Bias Amplification using Corpus-level Constraints

   [EMNLP17](http://aclweb.org/anthology/D/D17/D17-1323.pdf) speaker: DU, Yupei
   - Assumtion: the gender bias in test set is the same as in training set.
   - Methods: add a constrints in test set and solve it by ``Lagrangian Relaxation``

2. Generating Natural Answers by Incorporating Copying and Retrieving Mechanisms in Sequence-to-Sequence Learning

   [ACL17](http://aclweb.org/anthology/P/P17/P17-1019.pdf) LIU, Kang; ZHAO, Jun  speaker: XU, Hui Min
   - seq2seq + copying mechanism + retrieval from KB
   - P(Beijing) = P_{pr}(Beijing) + P_{co}(Beijing) + P_{re}(Beijing)
   - details:
     - how to use the facts from KB (M_{KB}: \{f_1, f_2, \ldots, f_n\})? (1) meaning, in the predict model. (2) position, in the copy and retrieval model (history acccumulated attention).
     - experiments: (1) build Q-A pairs using Q-A patterns. (2) GenQA + Baidu Zhidao
     - related work: (1) CopyNet (Gu et al., 2016); (2) GenQA (Yin et al., 2016)

3. TO READ

-  [Globally Normalized Reader](https://arxiv.org/pdf/1709.02828.pdf)
   QA, Speed
   
-  [Tensor2Tensor Transformers: New Deep Models for NLP]


4. An efficient framework for learning sentence representations 

   [ICLR18](https://openreview.net/pdf?id=rJvJXZb0W)
   
   - not novel 
   - well-writen
   - strong results
  
5. QANET: COMBINING LOCAL CONVOLUTION WITH GLOBAL SELF-ATTENTION FOR READING COMPREHENSION

   [ICLR18](https://openreview.net/forum?id=B14TlG-RW)
   
   - Conv + Attention
   - Data Augument (MT-backtranslation)
   
 6. Reinforced Co-Training
 
   [NAACL18](https://arxiv.org/pdf/1804.06035.pdf)
   
7. Attention Is All You Need

   - RNN-sequence
   - CNN-positional n-gram
   - Attention BOW
   
   - Attention + Position -> Multi-Head Attention
   - Position Encoding
   - Stack many layers -> RNN gate
  




