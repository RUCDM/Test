# 项目介绍
 本项目是中国人民大学信息学院大数据分析与智能实验室研制推出的一套基于深度学习的作文分类系统，采用多种
 不同的深度学习模型，具有作文分类，关键词提取，优美句子提取等功能。具有如下特点
 1. 速度快，提交作文的内容和标题，到返回分类结果所需实践仅１s，目前还在不断地优化中
 2. 分类准确率高，在我们的测试数据集上具有８０％以上的准确率，目前还在不断改善中
 3. 功能丰富，除了可以对文章进行分类，还具有提取关键词，提取优美句子的功能
# 不同深度学习模型分类性能对比
我们选择ubuntu操作系统作为测试环境,对传统的SVM模型和CNN等深度学习模型进行了效果对比，测试机的配置为：AMD A4-7300 APU
| Algorithm           | Precison      |    Recall    |  F-Measure   | settings                                  |
|:-------------------:|:-------------:|:------------:|:------------:|:-----------------------------------------:|
|docvec+title+LDA+SVM |0.801155292901 |0.803142857143|0.802147843826|128D doc2vec+128D title-word2vec+100D LDA  |
|docvec+SVM           |0.729639110528 |0.733142857143|0.731386787639|128D doc2vec                               |
|word2vec+CNN         |0.671994335198 |0.653571428571|0.662654859761|128D word2vec                              |
|Tf-idf + SVM         |0.672998320754 |0.433142857143|0.527065480119|13916D                                     |
# 相关论文
* [1]Tomas Mikolov, Kai Chen, Greg Corrado, and Jeffrey Dean. Efficient es-timation of word representations in vector space. CoRR, abs/1301.3781,2013.
* [2]Mikolov, T., Sutskever, I., Chen, K., Corrado, G. S., and Dean, J. (2013b). Distributedrepresentations of words and phrases and their compositionality. In Advances in Neural Information Processing Systems, pages 3111–3119.
* [3] Kim, Y. (2014). Convolutional Neural Networks for Sentence Classification. Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP 2014), 1746–1751.
