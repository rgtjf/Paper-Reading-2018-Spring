# Paper-Reading-2018-Spring

## Previous Edtions

- [Summer_Paper_Reading_2016](https://github.com/rgtjf/Summer_Paper_Reading_2016)
- [Paper-Reading-Third-Edition](https://github.com/rgtjf/Paper-Reading-Third-Edition)
- [Summer_Paper_Reading_2017](https://github.com/rgtjf/Summer_Paper_Reading_2017)

1. Men Also Like Shopping: Reducing Gender Bias Amplification using Corpus-level Constraints

    [EMNLP17](http://aclweb.org/anthology/D/D17/D17-1323.pdf) 
    speaker: DU, Yupei
    
    - Assumtion: the gender bias in test set is the same as in training set.
    - Methods: add a constrints in test set and solve it by ``Lagrangian Relaxation``

1. Globally Normalized Reader

    [arxiv](https://arxiv.org/pdf/1709.02828.pdf)

    - QA, Speed

1. Tensor2Tensor Transformers: New Deep Models for NLP

    [arxiv](./)

1. An efficient framework for learning sentence representations 

    [ICLR18](https://openreview.net/pdf?id=rJvJXZb0W)

    - not novel 
    - well-writen
    - strong results

1. QANET: COMBINING LOCAL CONVOLUTION WITH GLOBAL SELF-ATTENTION FOR READING COMPREHENSION

    [ICLR18](https://openreview.net/forum?id=B14TlG-RW)

    - Conv + Attention
    - Data Augument (MT-backtranslation)

1. Reinforced Co-Training

    [NAACL18](https://arxiv.org/pdf/1804.06035.pdf)

1. Attention Is All You Need

    - RNN-sequence
    - CNN-positional n-gram
    - Attention BOW
    - Attention + Position -> Multi-Head Attention
    - Position Encoding
    - Stack many layers -> RNN gate


## NLP Seminar

1. Generating Natural Answers by Incorporating Copying and Retrieving Mechanisms in Sequence-to-Sequence Learning

    [ACL17](http://aclweb.org/anthology/P/P17/P17-1019.pdf) LIU, Kang; ZHAO, Jun  speaker: XU, Hui Min

    - seq2seq + copying mechanism + retrieval from KB
    - P(Beijing) = P_{pr}(Beijing) + P_{co}(Beijing) + P_{re}(Beijing)
    - details:
    - how to use the facts from KB (M_{KB}: \{f_1, f_2, \ldots, f_n\})? (1) meaning, in the predict model. (2) position, in the copy and retrieval model (history acccumulated attention).
    - experiments: (1) build Q-A pairs using Q-A patterns. (2) GenQA + Baidu Zhidao
    - related work: (1) CopyNet (Gu et al., 2016); (2) GenQA (Yin et al., 2016)

1. Get To The Point: Summarization with Pointer-Generator Networks

    ACL17, Manning
    Speaker: LU, Xin Wu

    - pointer network for copy
    - coverage mechanism to avoid repeat
    - code is availble on GitHub

1. Coarse-to-Fine Question Answering for Long Documents

    ACL17, Eunsol Choi
    Speaker: XU, Hui Min

    - coarse: sentence selection, corpus => document summary
    - fine: answer generation document summary => answer

1. Neural Response Generation with Dynamic Vocabularies

    AAAI18, Beihang & MSRA
    Speaker: LU, Xin Wu

    - dynamic vocabulary construction: top K
    - pointer network: select? (not sure)
    - training? reinforcement

1. Ask the Right Questions_Active Question Reformulation with Reinforcement Learning

    ICLR18, Google
    Speaker: SHENG, Yi Xuan

     - Before QA system, reformulate the question (seq2seq)
     - After generating the condinates, select the answer (CNN)
     - Training: BiDAF + Reinforment

1. FAST AND ACCURATE READING COMPREHENSION BY COMBINING SELF-ATTENTION AND CONVOLUTION

    ICLR18, CMU, Google
    Speaker: SHENG, Yi Xuan

    - not novel, the idea is from transformer
    - good writing and strong experiments 

1. Towards Diverse and Natural Image Descriptions via a Conditional GAN

    ICCV17, CUHK
    Speaker: XIU, Yu Huan

1. Sentence Ordering and Coherence Modeling using Recurrent Neural Networks

    AAAI18, University of Michigan
    Speaker: ZHOU, Yun Xiao

    - set2seq
    - multi-hop set
    - eval in SICK

1. Learning Discourse-level Diversity for Neural Dialog Models using Conditional Variational Autoencoders

    ACL17, CMU
    Speaker: LU, Xin Wu

    - knowledge-guide VAE

1. KBQA Learning Question Answering over QA Corpora and Knowledge Bases

    VLDB17, FDU
    Speaker: XU, Hui Min

1. Dual Attention Networks for Multimodal Reasoning and Matching

    CVPR17, 
    Speaker: XIU, Yu Huan
