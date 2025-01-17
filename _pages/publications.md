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
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Preprint-Arxiv-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/llm-pruner.png' width="65%" class="fig">
        </div>
    </div>
    <dl class="pub-description">
        <dt class="ptitle">LLM-Pruner: On the Structural Pruning of Large Language Models</dt>
        <dd>- <b>Xinyin Ma</b>, Gongfan Fang, Xinchao Wang<br></dd>
        <dd>
            [<a class="plink" href="https://arxiv.org/abs/2305.11627" target="_blank">paper</a>]
            [<a class="plink" href="https://github.com/horseee/LLM-Pruner" target="_blank">code</a>] 
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Large language models (LLMs) have shown remarkable capabilities in language understanding and generation. However, such impressive capability typically comes with a substantial model size, which presents significant challenges in both the deployment, inference, and training stages. With LLM being a general-purpose task solver, we explore its compression in a task-agnostic manner, which aims to preserve the multi-task solving and language generation ability of the original LLM. One challenge to achieving this is the enormous size of the training corpus of LLM, which makes both data transfer and model post-training over-burdensome. Thus, we tackle the compression of LLMs within the bound of two constraints: being task-agnostic and minimizing the reliance on the original training dataset. Our method, named LLM-Pruner, adopts structural pruning that selectively removes non-critical coupled structures based on gradient information, maximally preserving the majority of the LLM's functionality. To this end, the performance of pruned models can be efficiently recovered through tuning techniques, LoRA, in merely 3 hours, requiring only 50K data. We validate the LLM-Pruner on three LLMs, including LLaMA, Vicuna, and ChatGLM, and demonstrate that the compressed models still exhibit satisfactory capabilities in zero-shot classification and generation.</p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-CVPR'23-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/Depgraph.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">DepGraph: Towards Any Structural Pruning</dt>
        <dd>- Gongfan Fang, <b>Xinyin Ma</b>, Mingli Song, Michael Bi Mi, Xinchao Wang<br></dd>
        <dd>- The IEEE/CVF Conference on Computer Vision and Pattern Recognition 2023</dd>
        <dd>
            [<a class="plink" href="https://arxiv.org/abs/2301.12900" target="_blank">paper</a>]
            [<a class="plink" href="https://github.com/VainF/Torch-Pruning" target="_blank">code</a>] 
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p>  Structural pruning enables model acceleration by removing structurally-grouped parameters from neural networks. However, the parameter-grouping patterns vary widely across different models, making architecture-specific pruners, which rely on manually-designed grouping schemes, non-generalizable to new architectures. In this work, we study a highly-challenging yet barely-explored task, any structural pruning, to tackle general structural pruning of arbitrary architecture like CNNs, RNNs, GNNs and Transformers. The most prominent obstacle towards this goal lies in the structural coupling, which not only forces different layers to be pruned simultaneously, but also expects all removed parameters to be consistently unimportant, thereby avoiding structural issues and significant performance degradation after pruning. To address this problem, we propose a general and fully automatic method, Dependency Graph(DepGraph), to explicitly model the dependency between layers and comprehensively group coupled parameters for pruning. In this work, we extensively evaluate our method on several architectures and tasks, including ResNe(X)t, DenseNet, MobileNet and Vision transformer for images, GAT for graph, DGCNN for 3D point cloud, alongside LSTM for language, and demonstrate that, even with a simple norm-based criterion, the proposed method consistently yields gratifying performances. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-IJCAI'22-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/PromptKD.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">Prompting to distill: Boosting Data-Free Knowledge Distillation via Reinforced Prompt</dt>
        <dd>- <b>Xinyin Ma</b>, Xinchao Wang, Gongfan Fang, Yongliang Shen, Weiming Lu <br></dd>
        <dd>- The 31st International Joint Conference on Artificial Intelligence and the 25th European Conference on Artificial Intelligence (IJCAI-ECAI 22), Oral (short presentation)</dd>
        <dd>
            [<a class="plink" href="https://www.ijcai.org/proceedings/2022/0596.pdf" target="_blank">paper</a>]
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Data-free knowledge distillation (DFKD) conducts knowledge distillation via eliminating the dependence of original training data, and has recently achieved impressive results in accelerating pre-trained language models. At the heart of DFKD is toreconstruct a synthetic dataset by invertingthe parameters of the uncompressed model. Prior DFKD approaches, however, havelargely relied on hand-crafted priors of the target data distribution for the reconstruction, which can be inevitably biased and often incompetent to capture the intrinsic distributions. To address this problem, we propose a prompt-based method, termed as PromptDFD, that allows us to take advantage of learned language priors, which effectively harmonizes the synthetic sentences to be semantically and grammatically correct. Specifically, PromptDFD leverages a pre-trained generative model to provide language priors and introduces a reinforced topic prompter to control data synthesis, making the generated samples thematically relevant and  semantically plausible, and thus friendly to downstream tasks. As shown in our experiments, the proposed method substantially improves the synthesis quality and achieves considerable improvements on distillation performance. In some cases, PromptDFD even gives rise to results on par with those from the data-driven knowledge distillation with access to the original training data. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-EMNLP'21-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/MuVER.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">MuVER: Improving First-Stage Entity Retrieval with Multi-View Entity Representations</dt>
        <dd>- <b>Xinyin Ma</b>, Yong Jiang, Nguyen Bach, Tao Wang, Zhongqiang Huang, Fei Huang, Weiming Lu <br></dd>
        <dd>- The 2021 Conference on Empirical Methods in Natural Language Processing (EMNLP 2021, short paper)</dd>
        <dd>
            [<a class="plink" href="https://aclanthology.org/2021.emnlp-main.205.pdf" target="_blank">paper</a>]
            [<a class="plink" href="https://github.com/alibaba-nlp/muver" target="_blank">code</a>] 
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Entity retrieval, which aims at disambiguating mentions to canonical entities from massive KBs, is essential for many tasks in natural language processing. Recent progress in entity retrieval shows that the dual-encoder structure is a powerful and efficient framework to nominate candidates if entities are only identified by descriptions. However, they ignore the property that meanings of entity mentions diverge in different contexts and are related to various portions of descriptions, which are treated equally in previous works. In this work, we propose Multi-View Entity Representations (MuVER), a novel approach for entity retrieval that constructs multi-view representations for entity descriptions and approximates the optimal view for mentions via a heuristic searching method. Our method achieves the state-of-the-art performance on ZESHEL and improves the quality of candidates on three standard Entity Linking datasets. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-EMNLP'20-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/ASDFD.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">Adversarial Self-Supervised Data-Free Distillation for Text Classification</dt>
        <dd>- <b>Xinyin Ma</b>, Yongliang Shen, Gongfan Fang, Chen Chen, Chenghao Jia, Weiming Lu <br></dd>
        <dd>- The 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP 2020)</dd>
        <dd>
            [<a class="plink" href="https://aclanthology.org/2020.emnlp-main.499.pdf" target="_blank">paper</a>]
            [<a class="plink" href="https://slideslive.com/38938706/adversarial-selfsupervised-datafree-distillation-for-text-classification" target="_blank">video</a>]
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Large pre-trained transformer-based language models have achieved impressive results on a wide range of NLP tasks. In the past few years, Knowledge Distillation(KD) has become a popular paradigm to compress a computationally expensive model to a resource-efficient lightweight model. However, most KD algorithms, especially in NLP, rely on the accessibility of the original training dataset, which may be unavailable due to privacy issues. To tackle this problem, we propose a novel two-stage data-free distillation method, named Adversarial self-Supervised Data-Free Distillation (AS-DFD), which is designed for compressing large-scale transformer-based models (e.g., BERT). To avoid text generation in discrete space, we introduce a Plug & Play Embedding Guessing method to craft pseudo embeddings from the teacher’s hidden knowledge. Meanwhile, with a self-supervised module to quantify the student’s ability, we adapt the difficulty of pseudo embeddings in an adversarial training manner. To the best of our knowledge, our framework is the first data-free distillation framework designed for NLP tasks. We verify the effectiveness of our method on several text classification datasets. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-ACL'21-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/LocateLabel.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">Locate and Label: A Two-stage Identifier for Nested Named Entity Recognition</dt>
        <dd>- Yongliang Shen, <b>Xinyin Ma</b>, Zeqi Tan, Shuai Zhang, Wen Wang, Weiming Lu <br></dd>
        <dd>- The 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (ACL 2021)</dd>
        <dd>
            [<a class="plink" href="https://aclanthology.org/2021.acl-long.216.pdf" target="_blank">paper</a>]
            [<a class="plink" href="https://github.com/tricktreat/locate-and-label" target="_blank">code</a>] 
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Named entity recognition (NER) is a well-studied task in natural language processing. Traditional NER research only deals with flat entities and ignores nested entities. The span-based methods treat entity recognition as a span classification task. Although these methods have the innate ability to handle nested NER, they suffer from high computational cost, ignorance of boundary information, under-utilization of the spans that partially match with entities, and difficulties in long entity recognition. To tackle these issues, we propose a two-stage entity identifier. First we generate span proposals by filtering and boundary regression on the seed spans to locate the entities, and then label the boundary-adjusted span proposals with the corresponding categories. Our method effectively utilizes the boundary information of entities and partially matched spans during training. Through boundary regression, entities of any length can be covered theoretically, which improves the ability to recognize long entities. In addition, many low-quality seed spans are filtered out in the first stage, which reduces the time complexity of inference. Experiments on nested NER datasets demonstrate that our proposed method outperforms previous state-of-the-art models. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-WWW'21-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/Trigger.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">A Trigger-Sense Memory Flow Framework for Joint Entity and Relation Extraction</dt>
        <dd>- Yongliang Shen, <b>Xinyin Ma</b>, Yechun Tang, Weiming Lu <br></dd>
        <dd>- The Web Conference 2021 (WWW 2021)</dd>
        <dd>
            [<a class="plink" href="https://dl.acm.org/doi/abs/10.1145/3442381.3449895" target="_blank">paper</a>]
            [<a class="plink" href="https://github.com/tricktreat/trimf" target="_blank">code</a>]
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Joint entity and relation extraction framework constructs a unified model to perform entity recognition and relation extraction simultaneously, which can exploit the dependency between the two tasks to mitigate the error propagation problem suffered by the pipeline model. Current efforts on joint entity and relation extraction focus on enhancing the interaction between entity recognition and relation extraction through parameter sharing, joint decoding, or other ad-hoc tricks (e.g., modeled as a semi-Markov decision process, cast as a multi-round reading comprehension task). However, there are still two issues on the table. First, the interaction utilized by most methods is still weak and uni-directional, which is unable to model the mutual dependency between the two tasks. Second, relation triggers are ignored by most methods, which can help explain why humans would extract a relation in the sentence. They’re essential for relation extraction but overlooked. To this end, we present a Trigger-Sense Memory Flow Framework (TriMF) for joint entity and relation extraction. We build a memory module to remember category representations learned in entity recognition and relation extraction tasks. And based on it, we design a multi-level memory flow attention mechanism to enhance the bi-directional interaction between entity recognition and relation extraction. Moreover, without any human annotations, our model can enhance relation trigger information in a sentence through a trigger sensor module, which improves the model performance and makes model predictions with better interpretation. Experiment results show that our proposed framework achieves state-of-the-art results by improves the relation F1 to 52.44% (+3.2%) on SciERC, 66.49% (+4.9%) on ACE05, 72.35% (+0.6%) on CoNLL04 and 80.66% (+2.3%) on ADE. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-IJCAI'20-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/Multihop.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">Multi-hop Reading Comprehension across Documents with Path-based Graph Convolutional Network</dt>
        <dd>- Zeyun Tang, Yongliang Shen, <b>Xinyin Ma</b>, Wei Xu, Jiale Yu, Weiming Lu <br></dd>
        <dd>- The Twenty-Ninth International Joint Conference on Artificial Intelligence (IJCAI 2020)</dd>
        <dd>
            [<a class="plink" href="https://www.ijcai.org/proceedings/2020/0540.pdf" target="_blank">paper</a>]
            [<a class="plink" href="https://www.ijcai.org/proceedings/2020/video/26636" target="_blank">video</a>]
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> Multi-hop reading comprehension across multiple documents attracts much attentions recently. In this paper, we propose a novel approach to tackle this multi-hop reading comprehension problem. Inspired by the human reasoning processing, we introduce a path-based graph with reasoning paths which extracted from supporting documents. The path-based graph can combine both the idea of the graph-based and path-based approaches, so it is better for multi-hop reasoning. Meanwhile, we propose Gated-GCN to accumulate evidences on the path-based graph, which contains a new question-aware gating mechanism to regulate the usefulness of information propagating across documents and add question information during reasoning. We evaluate our approach on WikiHop dataset, and our approach achieves the the-state-of-art accuracy against previous published approaches. Especially, our ensemble model surpasses the human performance by 4.2%. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>

<div class="publication">
    <div class='pub-image'>
        <div>
            <img src="https://img.shields.io/badge/Conference-IPM'20-blue" class="label"> <br>
            <img src='https://horseee.github.io/images/entitylink.png' width="100%" class="fig">
        </div>
    </div>  
    <dl class="pub-description">
        <dt class="ptitle">Enrich cross-lingual entity links for online wikis via multi-modal semantic matching</dt>
        <dd>- Weiming Lu, Peng Wang, <b>Xinyin Ma</b>, Wei Xu, Chen Chen <br></dd>
        <dd>- Information Processing & Management (IPM 2020)</dd>
        <dd>
            [<a class="plink" href="https://www.sciencedirect.com/science/article/abs/pii/S0306457319309094" target="_blank">paper</a>]
            <div class="link2">
                [<a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()">abstract</a>]
                <div class="abstract"  style="overflow: hidden; display: none;">  
                    <p> The task of enriching cross-lingual links is to find articles in different languages but representing the same real-world object between multilingual Wikis. In this paper, we propose a novel Multi-Modal Semantic Matching approach, called MMSM, to enrich cross-lingual links for online Wikis. Specifically, MMSM jointly trains two novel end-to-end neural matching models, Entity Description Matching Model and Entity Image Matching Model, which can utilize entity description and images for the cross-lingual entity matching. To the best of our knowledge, it is the first work to utilize multi-modal information to enrich cross-lingual entity links. In the experiments on three datasets CEMZH−ENEasy, CEMZH−ENChallenge and CEMFR−ENEasy, our approach gets the best performance compared with other baseline approaches. </p>
                </div>
            </div> 
        </dd>
    </dl>
</div>
 
