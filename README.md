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

1. ACL17-CAS-Generating Natural Answers by Incorporating Copying and Retrieving Mechanisms in Sequence-to-Sequence Learning

    speaker: XU, Hui Min

    - seq2seq + copying mechanism + retrieval from KB
    - P(Beijing) = P_{pr}(Beijing) + P_{co}(Beijing) + P_{re}(Beijing)
    - details:
    - how to use the facts from KB (M_{KB}: \{f_1, f_2, \ldots, f_n\})? (1) meaning, in the predict model. (2) position, in the copy and retrieval model (history acccumulated attention).
    - experiments: (1) build Q-A pairs using Q-A patterns. (2) GenQA + Baidu Zhidao
    - related work: (1) CopyNet (Gu et al., 2016); (2) GenQA (Yin et al., 2016)

    本文认为传统的QA针对问题仅返回一个知识实体是不友好的表达，因此提出一种可融入外部知识库的端到端神经网络模型，在Seq2Seq学习中整合了复制和检索机制，从而能产生一个包括了答案的完整句子。

1. ACL17-Manning-Get To The Point: Summarization with Pointer-Generator Networks

    Speaker: LU, Xin Wu

    本文针对长文本生成式摘要中出现的两个问题：（1）事实错误以及未登录词的问题（2）解码时生成重复句子。问题1作者提出结合point network来解决，问题2作者引入了Coverage mechanism来解决。

    - pointer network for copy
    - coverage mechanism to avoid repeat
    - code is availble on GitHub

1. ACL17-Eunsol Choi-Coarse-to-Fine Question Answering for Long Documents

    Speaker: Sheng, Yi Xuan

     本周我讲的是2017ACL长论文，旨在解决长文档的问答，主要分两个步骤：(1)粗粒度的快速的句子选择； (2)从选择的句子中进行更精确的答案选择。

    - coarse: sentence selection, corpus => document summary
    - fine: answer generation document summary => answer

1. AAAI18-MSRA-Neural Response Generation with Dynamic Vocabularies

    Speaker: LU, Xin Wu

    - dynamic vocabulary construction: top K
    - pointer network: select? (not sure)
    - training? reinforcement

    本文针对采用静态词表解码容易生成不相关回复以及解码效率过低的问题，提出了使用动态词表解码来解决。

1. ICLR18-Ask the Right Questions_Active Question Reformulation with Reinforcement Learning

    ICLR18, Google
    Speaker: Xu, Hui Min

     - Before QA system, reformulate the question (seq2seq)
     - After generating the condinates, select the answer (CNN)
     - Training: BiDAF + Reinforment

     这篇论文构造一个位于用户和QA环境之间的agent，agent利用强化学习方法学习重新构造问题，输入到QA环境中，从而引出最好的答案。

1. ICLR18-CMU-FAST AND ACCURATE READING COMPREHENSION BY COMBINING SELF-ATTENTION AND CONVOLUTION

    Speaker: SHENG, Yi Xuan

    这周我要讲的论文发表于ICLR2018, 本文主要贡献有两点：
    - 以往都是用rnn做Encoder Layer的编码，这篇文章为了加快阅读理解的训练速度，完全不用rnn，采用[convolution-layer + self-attention-layer + feed-forward-layer]的block来加快编码速度。
    - 因为编码速度加快，可以训练跟多的数据，采用机器翻译的方式去把文章翻译成法语和德语再翻译成英语，从而扩展了文章数据，来提高系统性能。

    - not novel, the idea is from transformer
    - good writing and strong experiments


1. ICCV17-CUHK-Towards Diverse and Natural Image Descriptions via a Conditional GAN

    Speaker: XIU, Yu Huan

    为了提高图像描述的多样性和自然性，本篇论文提出了基于条件生成对抗网络（CGAN）的模型，并结合强化学习中的策略梯度方法来生成图像描述。该方法不仅鼓励生成描述与图像视觉内容的保真度，而且鼓励模型产生多样、自然的描述。同时产生一个图像描述的评估器，该评估器的评估结果与人类评估结果大体上是一致的。

1. AAAI18-Michigan-Sentence Ordering and Coherence Modeling using Recurrent Neural Networks

    Speaker: ZHOU, Yun Xiao

    - set2seq
    - multi-hop set
    - eval in SICK

    本文发表于AAAI2018，提出了一个基于RNN的句子排序和连贯性建模的模型，其使用端到端的set-to-sequence框架，在得到文档的向量表示后，利用句子级别的pointer network对输入的句子进行选择，从而实现句子的排序。

1. ACL17-CMU-Learning Discourse-level Diversity for Neural Dialog Models using Conditional Variational Autoencoders

    Speaker: LU, Xin Wu

    本文针对采用静态词表解码容易生成不相关回复以及解码效率过低的问题，提出了使用动态词表解码来解决。

    - knowledge-guide VAE

1. VLDB17-FDU-KBQA Learning Question Answering over QA Corpora and Knowledge Bases

    Speaker: XU, Hui Min

    本文针对目前QA系统所用的基于规则/关键字/同义词的方法不能完全理解问题，提出一种基于亿级知识库和百万级QA语料库来学习了27M个问题模板。通过 问题 → 提取实体 → 问题抽象成模板 → 模板与谓词的对应关系 → 答案 来学习到问题的语义，并与知识库中RDF三元组映射。

1. CVPR17-Dual Attention Networks for Multimodal Reasoning and Matching

    Speaker: XIU, Yu Huan

    作者使用对偶注意网络（DAN）解决多模式推断（视觉问答，VAQ）和多模式匹配问题。本文提出的对偶注意网络同时利用视觉和文本注意机制来捕捉视觉和语言之间的细微相互作用。并且作者进行了广泛的实验，验证了DAN在结合视觉和语言方面的有效性，实现了关于VQA和图像文本匹配的公共基准的最新性能。

1. ACL18-Multi-Passage Machine Reading Comprehension with Cross-Passage Answer Verification

    SHENG, Yi Xuan

    这篇文章主要解决多passage的阅读理解问题，主要改进是在答案输出层，以往的论文只考虑了用pointer network定位答案的边界，本文除了定位答案边界，还加上了答案内容的建模，和Cross-Passage 的答案验证，在MS-MARCO上得到了ROUGE-L：46.66 BLEU-1：45.41，接近人类的水平(ROUGE-L：47 BLEU-1：46)

    - For Multi-Passage
    - Answer Boundary Prediction
    - Answer Content Modeling: use binary word loss
    - Answer Verification: check answers[]

1. ACL17-BridgingText and Knowledge by Learning Multi-Prototype Entity Mention Embedding

    XU, Hui Min

    在知识库和文本的联合表示中，歧义是个困扰的难题。同一个 mention 可能在不同的语境下表述不同实体，同一个实体又有多种 mention 表示。本文提出了一个新的表示方法，可以在一个联合空间学习 mention 和实体的表示，同时解决歧义问题。

1. ACL17-HIT-Selective Encoding for Abstractive Sentence Summarization

    LU, Xin Wu

    本文实现了一个句子级别的生成式摘要，本文作者在传统编码解码模型的基础上添加了编码选择层进行信息过滤，有效提高了摘要生成的质量。

1. ACL18-NTHU-A Unified Model for Extractive and Abstractive Summarization using Inconsistency Loss

    LU, Xin Wu

    这是我本周要讲的论文，发表在18年ACL会议上。本文提出在分层编码解码模型的基础上利用分层attention机制将抽取式与生成式结合。并提出了不一致性损失函数将两者结合提高生成质量。

1. IJCAI18-THU-Assigning PersonalityIdentity to a Chatting Machine for Coherent Conversation Generation

    ZHOU, Zhi Heng

    本文着重关注对话中机器人的身份一致性的问题，采用位置解码器挑选出从哪个位置开始解码，双向的解码器从前向和后向来生成身份属性一致的回答