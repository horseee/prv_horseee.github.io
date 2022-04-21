---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<script type="text/javascript" src="{{ base_path }}/assets/js/jquery-3.6.0.min.js"></script>

<div class="publication">
    <dl class="description">
        <dt class="ptitle">Prompting to distill: Boosting Data-Free Knowledge Distillation via Reinforced Prompt</dt>
        <dd><b>Xinyin Ma</b>, Xinchao Wang, Gongfan Fang, Yongliang Shen, Weiming Lu <br></dd>
        <dd>The 31st International Joint Conference on Artificial Intelligence and the 25th European Conference on Artificial Intelligence (IJCAI-ECAI 22), Oral (short presentation)</dd>
        <dd>
            [<a href="" target="_blank">paper</a>]
            [<a href="" target="_blank">code</a>]
            <div class="link2">[<a class="fakelink" onclick="$(this).siblings('.bibref').slideToggle()">bibtex</a>]
              <div class="bibref pre-white-space"  style="overflow: hidden; display: none;">
              </div>
            </div>  
            <div class="link2">[<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Data-free knowledge distillation (DFKD) conducts knowledge distillation via eliminating the dependence of original training data, and has recently achieved impressive results in accelerating pre-trained language models. At the heart of DFKD is toreconstruct a synthetic dataset by invertingthe parameters of the uncompressed model. Prior DFKD approaches, however, havelargely relied on hand-crafted priors of the target data distribution for the reconstruction, which can be inevitably biased and often incompetent to capture the intrinsic distributions. To address this problem, we propose a prompt-based method, termed as PromptDFD, that allows us to take advantage of learned language priors, which effectively harmonizes the synthetic sentences to be semantically and grammatically correct. Specifically, PromptDFD leverages a pre-trained generative model to provide language priors and introduces a reinforced topic prompter to control data synthesis, making the generated samples thematically relevant and  semantically plausible, and thus friendly to downstream tasks. As shown in our experiments, the proposed method substantially improves the synthesis quality and achieves considerable improvements on distillation performance. In some cases, PromptDFD even gives rise to results on par with those from the data-driven knowledge distillation with access to the original training data. </p>
                </div>
                (Note: The paper and the code will be released soon) 
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <dl class="description">
        <dt class="ptitle">Adversarial Self-Supervised Data-Free Distillation for Text Classification</dt>
        <dd><b>Xinyin Ma</b>, Yongliang Shen, Gongfan Fang, Chen Chen, Chenghao Jia, Weiming Lu <br></dd>
        <dd> Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP 2020)</dd>
        <dd>
            [<a href="https://aclanthology.org/2020.emnlp-main.499.pdf" target="_blank">paper</a>]
            [<a href="https://slideslive.com/38938706/adversarial-selfsupervised-datafree-distillation-for-text-classification" target="_blank">video</a>]
            <div class="link2">[<a class="fakelink" onclick="$(this).siblings('.bibref').slideToggle()">bibtex</a>]
              <div class="bibref pre-white-space"  style="overflow: hidden; display: none;">
              @inproceedings{ma-etal-2020-adversarial,
                  title = "{A}dversarial {S}elf-{S}upervised {D}ata-{F}ree {D}istillation for {T}ext {C}lassification",
                  author = "Ma, Xinyin  and
                    Shen, Yongliang  and
                    Fang, Gongfan  and
                    Chen, Chen  and
                    Jia, Chenghao  and
                    Lu, Weiming",
                  booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
                  month = nov,
                  year = "2020",
                  address = "Online",
                  publisher = "Association for Computational Linguistics",
                  url = "https://aclanthology.org/2020.emnlp-main.499",
                  doi = "10.18653/v1/2020.emnlp-main.499",
                  pages = "6182--6192",
                  abstract = "Large pre-trained transformer-based language models have achieved impressive results on a wide range of NLP tasks. In the past few years, Knowledge Distillation(KD) has become a popular paradigm to compress a computationally expensive model to a resource-efficient lightweight model. However, most KD algorithms, especially in NLP, rely on the accessibility of the original training dataset, which may be unavailable due to privacy issues. To tackle this problem, we propose a novel two-stage data-free distillation method, named Adversarial self-Supervised Data-Free Distillation (AS-DFD), which is designed for compressing large-scale transformer-based models (e.g., BERT). To avoid text generation in discrete space, we introduce a Plug {\&} Play Embedding Guessing method to craft pseudo embeddings from the teacher{'}s hidden knowledge. Meanwhile, with a self-supervised module to quantify the student{'}s ability, we adapt the difficulty of pseudo embeddings in an adversarial training manner. To the best of our knowledge, our framework is the first data-free distillation framework designed for NLP tasks. We verify the effectiveness of our method on several text classification datasets.",
              }
              </div>
            </div>  
            <div class="link2">[<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Large pre-trained transformer-based language models have achieved impressive results on a wide range of NLP tasks. In the past few years, Knowledge Distillation(KD) has become a popular paradigm to compress a computationally expensive model to a resource-efficient lightweight model. However, most KD algorithms, especially in NLP, rely on the accessibility of the original training dataset, which may be unavailable due to privacy issues. To tackle this problem, we propose a novel two-stage data-free distillation method, named Adversarial self-Supervised Data-Free Distillation (AS-DFD), which is designed for compressing large-scale transformer-based models (e.g., BERT). To avoid text generation in discrete space, we introduce a Plug & Play Embedding Guessing method to craft pseudo embeddings from the teacher’s hidden knowledge. Meanwhile, with a self-supervised module to quantify the student’s ability, we adapt the difficulty of pseudo embeddings in an adversarial training manner. To the best of our knowledge, our framework is the first data-free distillation framework designed for NLP tasks. We verify the effectiveness of our method on several text classification datasets. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

1. MuVER: Improving First-Stage Entity Retrieval with Multi-View Entity Representations, EMNLP2021(Short), [[pdf]](https://arxiv.org/abs/2109.05716)  
  **Xinyin Ma**, Yong Jiang, Nguyen Bach, Tao Wang, Zhongqiang Huang, Fei Huang, Weiming Lu
4. Locate and Label: A Two-stage Identifier for Nested Named Entity Recognition, ACL2021, [[pdf]](https://arxiv.org/abs/2105.06804)  
  Yongliang Shen, **Xinyin Ma**, Zeqi Tan, Shuai Zhang, Wen Wang, Weiming Lu
5. A Trigger-Sense Memory Flow Framework for Joint Entity and Relation Extraction, WWW2021, [[pdf]](https://dl.acm.org/doi/abs/10.1145/3442381.3449895)  
  Yongliang Shen, **Xinyin Ma**, Yechun Tang, Weiming Lu
6. Enrich cross-lingual entity links for online wikis via multi-modal semantic matching, IPM 2020, [[pdf]](https://www.sciencedirect.com/science/article/abs/pii/S0306457319309094)  
  Weiming Lu, Peng Wang, **Xinyin Ma**, Wei Xu, Chen Chen
7. Multi-hop Reading Comprehension across Documents with Path-based Graph Convolutional Network,  IJCAI2020, [[pdf]](https://arxiv.org/abs/2006.06478)  
  Zeyun Tang, Yongliang Shen, **Xinyin Ma**, Wei Xu, Jiale Yu, Weiming Lu
