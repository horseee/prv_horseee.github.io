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
        <dd>The 31st International Joint Conference on Artificial Intelligence and the 25th European Conference on Artificial Intelligence (IJCAI-22), Oral (short presentation)</dd>
        <dd> The paper and the code will be released soon</dd>
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
            </div>       
        </dd>
    </dl>
</div>

1.  The paper and the code will be released soon.  
  **Xinyin Ma**, Xinchao Wang, Gongfan Fang, Yongliang Shen, Weiming Lu  
2. Adversarial Self-Supervised Data-Free Distillation for Text Classification, EMNLP2020, [[pdf]](https://arxiv.org/abs/2010.04883)  
  **Xinyin Ma**, Yongliang Shen, Gongfan Fang, Chen Chen, Chenghao Jia, Weiming Lu
3. MuVER: Improving First-Stage Entity Retrieval with Multi-View Entity Representations, EMNLP2021(Short), [[pdf]](https://arxiv.org/abs/2109.05716)  
  **Xinyin Ma**, Yong Jiang, Nguyen Bach, Tao Wang, Zhongqiang Huang, Fei Huang, Weiming Lu
4. Locate and Label: A Two-stage Identifier for Nested Named Entity Recognition, ACL2021, [[pdf]](https://arxiv.org/abs/2105.06804)  
  Yongliang Shen, **Xinyin Ma**, Zeqi Tan, Shuai Zhang, Wen Wang, Weiming Lu
5. A Trigger-Sense Memory Flow Framework for Joint Entity and Relation Extraction, WWW2021, [[pdf]](https://dl.acm.org/doi/abs/10.1145/3442381.3449895)  
  Yongliang Shen, **Xinyin Ma**, Yechun Tang, Weiming Lu
6. Enrich cross-lingual entity links for online wikis via multi-modal semantic matching, IPM 2020, [[pdf]](https://www.sciencedirect.com/science/article/abs/pii/S0306457319309094)  
  Weiming Lu, Peng Wang, **Xinyin Ma**, Wei Xu, Chen Chen
7. Multi-hop Reading Comprehension across Documents with Path-based Graph Convolutional Network,  IJCAI2020, [[pdf]](https://arxiv.org/abs/2006.06478)  
  Zeyun Tang, Yongliang Shen, **Xinyin Ma**, Wei Xu, Jiale Yu, Weiming Lu
