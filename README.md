# Causal-Inference-for-Recommendation
A comprehensive repository featuring research works on causal inference for recommender systems, including both academic papers and their corresponding code implementations :fire:. For any inquiries or contributions, please contact hsluo2000@buaa.edu.cn or hsluo2000@gmail.com. We welcome any interesting papers or code related to this field. If you find this repository useful to your research or work, we would greatly appreciate a star on the repository. :heart:


[stars-img]: https://img.shields.io/github/stars/Chrissie-Law/Causal-Inference-for-Recommendation?color=yellow
[stars-url]: https://github.com/Chrissie-Law/Causal-Inference-for-Recommendation/stargazers
[fork-img]: https://img.shields.io/github/forks/Chrissie-Law/Causal-Inference-for-Recommendation?color=lightblue&label=fork
[fork-url]: https://github.com/Chrissie-Law/Causal-Inference-for-Recommendation/network/members
[CI4RS-url]: https://github.com/Chrissie-Law/Causal-Inference-for-Recommendation

[![GitHub stars][stars-img]][stars-url]
[![GitHub forks][fork-img]][fork-url]

If this repository or our survey paper is beneficial for your work, please cite: 
```
@article{luo2024ci4rs,
  title = {A survey on causal inference for recommendation},
  journal = {The Innovation},
  volume = {5},
  number = {2},
  pages = {100590},
  year = {2024},
  issn = {2666-6758},
  doi = {https://doi.org/10.1016/j.xinn.2024.100590},
  url = {https://www.cell.com/the-innovation/fulltext/S2666-6758(24)00028-6},
  author = {Luo, Huishi and Zhuang, Fuzhen and Xie, Ruobing and Zhu, Hengshu and Wang, Deqing and An, Zhulin and Xu, Yongjun}
}
```
Due to space limitations in the official publication in *[The Innovation](https://doi.org/10.1016/j.xinn.2024.100590)*, some figures and complete bibliographic tables are included in the supplemental material, which may be inconvenient for reading. **We strongly recommend consulting our [arXiv version](https://arxiv.org/pdf/2303.11666) :sparkles: of the paper for reading**, where all figures and bibliographic tables are positioned near the relevant text in the main document, significantly enhancing readability.

## Usage Guide

This repository offers a systematic review of research papers in the field of causal inference for recommendation systems, similar to the structure of the original survey. We categorize all works into three main types based on the causal inference theories they employ:

- **PO-based (Potential Outcome)**
- **SCM-based (Structural Causal Model)**
- **General Counterfactuals-based**

The comprehensive taxonomy is illustrated in the figure below. In addition, we have summarized the specific application problems that these works address within recommendation systems, which are listed in the"Issue of concern" column of our tables. You can use the search function of this web page to quickly find works of interest.

<div align="center">
    <figure>
        <img src="./pic/figure2.jpg" width="100%" alt="Strategies of the causal inference for recommendation">
        <figcaption>Figure 1: Strategies of the Causal Inference for Recommendation</figcaption>
    </figure>
</div>



## Project Updates

This repository is actively updated with the latest research papers up to early 2024. Updates will continue with new publications on causal inference for recommendation systems. Stay tuned!

## Bookmarks <span id="bookmarks"></span>
- [Survey Papers](#survey-papers)
- [PO-based Methods](#po-based-methods)
  - [Propensity Score Strategy](#propensity-score-strategy)
  - [Causal Effect Strategy](#causal-effect-strategy)
- [SCM-based Methods](#scm-based-methods)
- [General Counterfactuals-based Methods](#general-counterfactuals-based-methods)

## Survey Papers
| **Year**   | **Title**                                                                                     |  **Venue**    |                                       **Paper**                                            | **Code** |
| ---- |----------------------------------------------------------------------------------|:--------:|:---------------------------------------------------------------------------------:|:----:|
| 2023  | **A Survey on Causal Inference for Recommendation (Ours)**   |  arXiv    |                   [Link](https://arxiv.org/pdf/2303.11666.pdf)                    | [Link](https://github.com/Chrissie-Law/Causal-Inference-for-Recommendation)     |
| 2022  |  **Causal Inference in Recommender Systems: A Survey and Future Directions**  |  arXiv    | [Link](https://arxiv.org/pdf/2208.12397)  | -  |
| 2022 |  **On the opportunity of causal learning in recommendation systems: Foundation, estimation, prediction and challenges** |  IJCAI    | [Link](https://arxiv.org/pdf/2201.06716)  | - |
| 2023 | **Causal Inference for Recommendation: Foundations, Methods and Applications** |  arXiv    |  [Link](https://arxiv.org/pdf/2301.04016) | - |
| 2023 | **Causal Inference in Recommender Systems: A Survey of Strategies for Bias Mitigation, Explanation, and Generalization** |  arXiv    | [Link](https://arxiv.org/pdf/2301.00910) | - |

### Distinctive Features of Our Work
Our study on causal inference in recommender systems is distinguished by the following aspects:

* **Theoretically coherent classification framework from a causal perspective.** We adopts a more nuanced and theory-driven classification of causal recommender systems, categorizing algorithms into PO-based (Potential Outcome), SCM-based (Structural Causal Model), and general counterfactuals-based. This taxonomy offers a more structured and holistic understanding of causal theories, beneficial especially for newcomers in causal inference.
* **Evolution of Causal Methods in Recommender Systems.** We trace the developmental trajectory of the integration between prevalent causal inference theories and recommender systems.
* **Up-to-Date Collection and Review.** Our survey encompasses a comprehensive collection of recent works, as illustrated below.


<div align="center">
    <img src="./pic/paper_year_cate_rev.png" width="80%" alt="Distribution of publications on causal recommendations by year and framework">
    <p><strong>Figure 2:</strong> Distribution of publications on causal recommendations by year and framework, <br>focusing exclusively on specific industrial algorithms and excluding fundamental theory discussions.</p>
</div>



[Back](#bookmarks-)

## PO-based Methods

### Propensity score strategy

<div align="center">
    <img src="./pic/figure4.jpg" width="80%" alt="Evolutionary Timeline of Propensity Score Strategies in Recommendations">
    <p><strong>Figure 3:</strong> Evolutionary Timeline of Propensity Score Strategies in Recommendations.</p>
</div>



<table>
  <thead>
    <tr style="text-align: center;">
      <th>Category</th>
      <th>Model</th>
      <th>Causal inference method</th>
      <th>Base model</th>
      <th>Issue of concern</th>
      <th>Year</th>
      <th>Title</th>
      <th>Venue</th>
      <th>Paper Link</th>
      <th>Code Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="6">Approach Inspired by Propensity Score</td>
      <td>ExpoMF</td>
      <td>Propensity score</td>
      <td>Matrix factorization</td>
      <td>Exposure bias</td>
      <td>2016</td>
      <td>Modeling User Exposure in Recommendation</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/2872427.2883090">Link</a></td>
      <td><a href="https://github.com/dawenl/expo-mf">Link</a></td>
    </tr>
    <tr>
      <td>SERec</td>
      <td>Propensity score</td>
      <td>Matrix factorization</td>
      <td>Social Rec</td>
      <td>2018</td>
      <td>Collaborative Filtering with Social Exposure: A Modular Approach to Social Recommendation</td>
      <td>AAAI</td>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/11835">Link</a></td>
      <td><a href="https://github.com/99731/SERec">Link</a></td>
    </tr>
    <tr>
      <td>Dcf</td>
      <td>Propensity score</td>
      <td>Matrix factorization</td>
      <td>Unobserved confounding bias</td>
      <td>2020</td>
      <td>Causal Inference for Recommender Systems</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3383313.3412225">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CNFI</td>
      <td>Propensity score</td>
      <td>MF</td>
      <td>Implicit feedback</td>
      <td>2021</td>
      <td>Causal neural fuzzy inference modeling of missing data in implicit recommendation system</td>
      <td>KBS</td>
      <td><a href="https://www.sciencedirect.com/science/article/pii/S0950705120308078">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>IOBM</td>
      <td>Propensity score</td>
      <td>Bi-LSTM</td>
      <td>Interactional observation bias</td>
      <td>2021</td>
      <td>Adapting Interactional Observation Embedding for Counterfactual Learning to Rank</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/10.1145/3404835.3462901">Link</a></td>
      <td><a href="https://github.com/Keytoyze/Interactional-Observation-Based-Model">Link</a></td>
    </tr>
    <tr>
      <td>CCL</td>
      <td>Propensity score</td>
      <td>(custom-designed)</td>
      <td>Unobserved confounding bias</td>
      <td>2023</td>
      <td>Contrastive Counterfactual Learning for Causality-aware Interpretable Recommender Systems</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3583780.3614823">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
        <td rowspan="20">Approach with Inverse Propensity Score (IPS)</td>
        <td>MF-IPS</td>
        <td>IPS, SNIPS</td>
        <td>Matrix factorization</td>
        <td>Selection bias</td>
        <td>2016</td>
        <td>Recommendations as Treatments: Debiasing Learning and Evaluation</td>
        <td>JMLR</td>
        <td><a href="http://proceedings.mlr.press/v48/schnabel16.html?ref=https://githubhelp.com">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>PBM</td>
        <td>IPS</td>
        <td>SVM_Rank</td>
        <td>Position bias</td>
        <td>2017</td>
        <td>Unbiased Learning-to-Rank with Biased Feedback</td>
        <td>WSDM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3018661.3018699">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>PieceNCIS, PointNCIS</td>
        <td>CIPS, SNIPS</td>
        <td>-</td>
        <td>Offline A/B testing</td>
        <td>2018</td>
        <td>Offline A/B Testing for Recommender Systems</td>
        <td>WSDM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3159652.3159687">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>-</td>
        <td>IPS</td>
        <td>(reinforcement learning)</td>
        <td>Fairness</td>
        <td>2018</td>
        <td>Towards a Fair Marketplace: Counterfactual Evaluation of the trade-off between Relevance, Fairness & Satisfaction in Recommendation Systems</td>
        <td>CIKM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3269206.3272027">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>Multi-IPW</td>
        <td>IPS</td>
        <td>Multi-task DNN</td>
        <td>Selection bias</td>
        <td>2019</td>
        <td>Large-scale Causal Approaches to Debiasing Post-click Conversion Rate Estimation with Multi-task Learning</td>
        <td>WWW</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3366423.3380037">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>CPBM</td>
        <td>IPS</td>
        <td>SVM-Rank</td>
        <td>Selection bias</td>
        <td>2019</td>
        <td>Intervention Harvesting for Context-Dependent Examination-Bias Estimation</td>
        <td>SIGIR</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3331184.3331238">Link</a></td>
        <td><a href="https://github.com/fzc621/CondPropEst">Link</a></td>
      </tr>
      <tr>
        <td>ULRMF,ULBPR</td>
        <td>IPS, SNIPS, ATE</td>
        <td>Matrix factorization</td>
        <td>Uplift</td>
        <td>2019</td>
        <td>Uplif-based Evaluation and Optimization of Recommenders</td>
        <td>RecSys</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3298689.3347018">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>DLCE</td>
        <td>CIPS</td>
        <td>Matrix factorization</td>
        <td>Unobserved confoundeing bias</td>
        <td>2020</td>
        <td>Unbiased Learning for the Causal Effect of Recommendation</td>
        <td>RecSys</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3383313.3412261">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>Rel-MF</td>
        <td>CIPS</td>
        <td>Matrix factorization</td>
        <td>Unobserved confoundeing bias</td>
        <td>2020</td>
        <td>Unbiased Recommender Learning from Missing-Not-At-Random Implicit Feedback</td>
        <td>WSDM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3336191.3371783">Link</a></td>
        <td><a href="https://github.com/usaito/unbiased-implicit-rec">Link</a></td>
      </tr>
      <tr>
        <td>-</td>
        <td>IPS</td>
        <td>Multi-task MLP</td>
        <td>Observed confounding bias</td>
        <td>2020</td>
        <td>Deconfounding User Satisfaction Estimation from Response Rate Bias</td>
        <td>RecSys</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3383313.3412208">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>RIPS</td>
        <td>RIPS</td>
        <td>(model-agnostic)</td>
        <td>Slate Rec</td>
        <td>2020</td>
        <td>Counterfactual Evaluation of Slate Recommendations with Sequential Reward Interactions</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3394486.3403229">Link</a></td>
        <td><a href="https://github.com/spotify-research/RIPS_KDD2020">Link</a></td>
      </tr>
      <tr>
        <td>ACL</td>
        <td>IPS</td>
        <td>(adversarial learning)</td>
        <td>Identifiability</td>
        <td>2020</td>
        <td>Adversarial Counterfactual Learning and Evaluation for Recommender System</td>
        <td>NeurIPS</td>
        <td><a href="https://proceedings.neurips.cc/paper/2020/hash/9cd013fe250ebffc853b386569ab18c0-Abstract.html">Link</a></td>
        <td><a href="https://github.com/StatsDLMathsRecomSys/Adversarial-Counterfactual-Learning-and-Evaluation-for-Recommender-System">Link</a></td>
      </tr>
      <tr>
        <td>UR-IPW</td>
        <td>SNIPS</td>
        <td>Multi-task MLP</td>
        <td>Post-click revisit effect</td>
        <td>2021</td>
        <td>User Retention: A Causal Approach with Triple Task Modeling</td>
        <td>IJCAI</td>
        <td><a href="https://www.ijcai.org/proceedings/2021/468">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>-</td>
        <td>IPS</td>
        <td>model-agnostic</td>
        <td>Domain bias</td>
        <td>2021</td>
        <td>Debiasing Learning based Cross-domain Recommendation</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3447548.3467067">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>CBDF</td>
        <td>IPS</td>
        <td>(reinforcement learning)</td>
        <td>Delayed feedback</td>
        <td>2021</td>
        <td>Counterfactual Reward Modification for Streaming Recommendation with Delayed Feedback</td>
        <td>SIGIR</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462892">Link</a></td>
        <td><a href="https://github.com/hnjia00/Delayed-Feedback">Link</a></td>
      </tr>
      <tr>
        <td>RD&BRD</td>
        <td>IPS /DR /AutoDebias</td>
        <td>Matrix factorization</td>
        <td>Unobserved confoundeing bias</td>
        <td>2022</td>
        <td>Addressing Unmeasured Confounder for Recommendation with Sensitivity Analysis</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539240">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>CET</td>
        <td>IPS</td>
        <td>BERT</td>
        <td>False negative</td>
        <td>2022</td>
        <td>Hard Negatives or False Negatives: Correcting Pooling Bias in Training Neural Ranking Models</td>
        <td>CIKM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3511808.3557343">Link</a></td>
        <td><a href="https://github.com/caiyinqiong/Coupled_Estimation_Technique">Link</a></td>
      </tr>
      <tr>
        <td>CAFL</td>
        <td>IPS</td>
        <td>Matrix factorization</td>
        <td>Feedback loop</td>
        <td>2022</td>
        <td>Breaking Feedback Loops in Recommender Systems with Causal Inference</td>
        <td>arXiv</td>
        <td><a href="https://arxiv.org/abs/2207.01616">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>RIIPS</td>
        <td>RIIPS</td>
        <td>Two-tower structure</td>
        <td>Selection bias</td>
        <td>2022</td>
        <td>Practical Counterfactual Policy Learning for Top-K Recommendations</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539295">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>DENC</td>
        <td>IPS</td>
        <td>(custom-designed)</td>
        <td>Selection bias</td>
        <td>2023</td>
        <td>Be Causal: De-Biasing Social Network Confounding in Recommendation</td>
        <td>TKDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3533725">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td rowspan="10">Approach with Doubly Robust</td>
        <td>Propensity-free DR</td>
        <td>DR</td>
        <td>FFM</td>
        <td>Selection bias</td>
        <td>2019</td>
        <td>Improving Ad Click Prediction by Considering Non-displayed Events</td>
        <td>CIKM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3357384.3358058">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>DR-JL</td>
        <td>DR</td>
        <td>MF</td>
        <td>Selection Bias</td>
        <td>2019</td>
        <td>Doubly Robust Joint Learning for Recommendation on Data Missing Not at Random</td>
        <td>ICML</td>
        <td><a href="https://proceedings.mlr.press/v97/wang19n.html">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>Multi-DR</td>
        <td>DR</td>
        <td>Multi-task MLP</td>
        <td>Selection bias</td>
        <td>2020</td>
        <td>Large-scale Causal Approaches to Debiasing Post-click Conversion Rate Estimation with Multi-task Learning</td>
        <td>WWW</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3366423.3380037">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>MRDR-DL</td>
        <td>MRDR</td>
        <td>Matrix factorization</td>
        <td>Selection bias</td>
        <td>2021</td>
        <td>Enhanced Doubly Robust Learning for Debiasing Post-Click Conversion Rate Estimation</td>
        <td>SIGIR</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462917">Link</a></td>
        <td><a href="https://github.com/guosyjlu/MRDR-DL">Link</a></td>
      </tr>
      <tr>
        <td>Cascade-DR</td>
        <td>Cascade-DR</td>
        <td>Matrix factorization</td>
        <td>High variance of RIPS</td>
        <td>2022</td>
        <td>Doubly Robust Off-Policy Evaluation for Ranking Policies under the Cascade Behavior Model</td>
        <td>WSDM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3488560.3498380">Link</a></td>
        <td><a href="https://github.com/aiueola/wsdm2022-cascade-dr">Link</a></td>
      </tr>
      <tr>
        <td>ASPIRE</td>
        <td>DR, ATE</td>
        <td>LightGBM</td>
        <td>Uplift</td>
        <td>2022</td>
        <td>ASPIRE: Air Shipping Recommendation for E-commerce Products via Causal Inference Framework</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539197">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>DRIB</td>
        <td>DR</td>
        <td>Matrix factorization</td>
        <td>Unobserved confoundeing bias</td>
        <td>2022</td>
        <td>Towards Unbiased and Robust Causal Ranking for Recommender Systems</td>
        <td>WSDM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3488560.3498521">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>DR-BIAS, DR-MSE</td>
        <td>DR</td>
        <td>FM</td>
        <td>Selection Bias</td>
        <td>2022</td>
        <td>A Generalized Doubly Robust Learning Framework for Debiasing Post-Click Conversion Rate Prediction</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539270">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>CDR</td>
        <td>DR</td>
        <td>MF</td>
        <td>Selection bias</td>
        <td>2023</td>
        <td>CDR: Conservative Doubly Robust Learning for Debiased Recommendation</td>
        <td>CIKM</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3583780.3614805">Link</a></td>
        <td>-</td>
      </tr>
      <tr>
        <td>CF-MTL</td>
        <td>CATE, IPS, DR</td>
        <td>(custom-designed)</td>
        <td>Personalized incentive policy</td>
        <td>2023</td>
        <td>Who Should Be Given Incentives? Counterfactual Optimal Treatment Regimes Learning for Recommendation</td>
        <td>KDD</td>
        <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599550">Link</a></td>
        <td><a href="https://github.com/haoxuanli-pku/KDD23-Counterfactual">Link</a></td>
      </tr>
  </tbody>
</table>

[Back](#bookmarks-)

### Causal effect strategy

<table>
  <thead>
    <tr style="text-align: center;">
      <th>Category</th>
      <th>Model</th>
      <th>Causal inference method</th>
      <th>Base model</th>
      <th>Issue of concern</th>
      <th>Year</th>
      <th>Title</th>
      <th>Venue</th>
      <th>Paper Link</th>
      <th>Code Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5">Causal Effect for Uplift</td>
      <td>ULRMF, ULBPR</td>
      <td>IPS, SNIPS, ATE</td>
      <td>MF</td>
      <td rowspan="5">Uplift</td>
      <td>2019</td>
      <td>Uplift-based evaluation and optimization of recommenders</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3298689.3347018">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>CATE</td>
      <td>Xgboost</td>
      <td>2020</td>
      <td>Free Lunch! Retrospective Uplift Modeling for Dynamic Promotions Recommendation within ROI Constraints</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3383313.3412215">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>AUUC-max</td>
      <td>CATE</td>
      <td>Linear/Wide & Deep</td>
      <td>2021</td>
      <td>Uplift Modeling with Generalization Guarantees</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3447548.3467395">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CausCF</td>
      <td>CATE</td>
      <td>Matrix factorization</td>
      <td>2021</td>
      <td>Causally Attentive Collaborative Filtering</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482070">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>ASPIRE</td>
      <td>DR, ATE</td>
      <td>LightGBM</td>
      <td>2022</td>
      <td>ASPIRE: Air Shipping Recommendation for E-commerce Products via Causal Inference Framework</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539197">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td rowspan="6">Causal Effect beyond Uplift</td>
      <td>-</td>
      <td>ITE</td>
      <td>Linear/regularized kernel methods</td>
      <td>Domain adaptation</td>
      <td>2017</td>
      <td>Predicting Counterfactuals from Large Historical Data and Small Randomized Trials</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3041021.3054190">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CausE</td>
      <td>ITE</td>
      <td>MF</td>
      <td>Domain adaptation</td>
      <td>2018</td>
      <td>Causal Embeddings for Recommendation</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3240323.3240360">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>TE</td>
      <td>Structural state-space model</td>
      <td>Causal effect of a new track release</td>
      <td>2020</td>
      <td>Inferring the Causal Impact of New Track Releases on Music Recommendation Platforms through Counterfactual Predictions</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3383313.3418491">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CACF</td>
      <td>ITE</td>
      <td>(custom-designed)</td>
      <td>Unobserved confounding bias</td>
      <td>2021</td>
      <td>Causally Attentive Collaborative Filtering</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482070">Link</a></td>
      <td><a href="https://github.com/JingsenZhang/CACF">Link</a></td>
    </tr>
    <tr>
      <td>MCRec</td>
      <td>CATE</td>
      <td>DIN</td>
      <td>Device-cloud collaborative recommendation</td>
      <td>2022</td>
      <td>Device-cloud Collaborative Recommendation via Meta Controller</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539181">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>LRIR</td>
      <td>ITE, ATE</td>
      <td>(custom-designed)</td>
      <td>Disability employment</td>
      <td>2022</td>
      <td>What is the Most Effective Intervention to Increase Job Retention for this Disabled Worker?</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539026">Link</a></td>
      <td>-</td>
    </tr>
  </tbody>
</table>


[Back](#bookmarks-)

## SCM-based Methods

<div align="center">
    <img src="./pic/figure8.jpg" width="80%" alt="Separate-learning-counterfactual-inference in SCM-based causal inference">
    <p><strong>Figure 4:</strong> Separate-learning-counterfactual-inference, a common pattern of SCM-based causal inference for recommender systems,<br>learns causal effect with a separate structure or multi-task framework and performs counterfactual inference during testing.</p>
</div>


<table>
  <thead>
    <tr style="text-align: center;">
      <th>Category</th>
      <th>Model</th>
      <th>Causal inference method</th>
      <th>Base model</th>
      <th>Issue of concern</th>
      <th>Year</th>
      <th>Title</th>
      <th>Venue</th>
      <th>Paper Link</th>
      <th>Code Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">Causal Recommendation with Collider Structure</td>
      <td>DICE</td>
      <td>(causal view)</td>
      <td>Matrix factorization (multi-task)</td>
      <td>Popularity bias</td>
      <td>2021</td>
      <td>Disentangling User Interest and Conformity for Recommendation with Causal Embedding</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3442381.3449788">Link</a></td>
      <td><a href="https://github.com/tsinghua-fib-lab/DICE">Link</a></td>
    </tr>
    <tr>
      <td>CIGC</td>
      <td>Intervention on the cause factor</td>
      <td>LightGCN</td>
      <td>GCN model retraining</td>
      <td>2022</td>
      <td>Causal Incremental Graph Convolution for Recommender System Retraining</td>
      <td>TNNLS</td>
      <td><a href="https://ieeexplore.ieee.org/abstract/document/9737000/">Link</a></td>
      <td><a href="https://github.com/Dingseewhole/CI_LightGCN_master">Link</a></td>
    </tr>
    <tr>
      <td>MGCE</td>
      <td>(causal view)</td>
      <td>linear GCN</td>
      <td>Popularity bias</td>
      <td>2024</td>
      <td>Multimodal Graph Causal Embedding for Multimedia-Based Recommendation</td>
      <td>TKDE</td>
      <td><a href="https://ieeexplore.ieee.org/abstract/document/10587159/">Link</a></td>
      <td><a href="https://github.com/shuaiyangli/MGCE">Link</a></td>
    </tr>
    <tr>
      <td>DDCE</td>
      <td>(causal view)</td>
      <td>(self-designed)</td>
      <td>Popularity bias</td>
      <td>2023</td>
      <td>Dual disentanglement of user–item interaction for recommendation with causal embedding</td>
      <td>IPM</td>
      <td><a href="https://www.sciencedirect.com/science/article/pii/S0306457323001930">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td rowspan="6">Causal Recommendation with Mediator Structure</td>
      <td>-</td>
      <td>Mediation analysis</td>
      <td>-</td>
      <td>Effect of social presence</td>
      <td>2011</td>
      <td>The Influence of Social Presence on Customer Intention to Reuse Online Recommender Systems: The Roles of Personalization and Product Type</td>
      <td>IJEC</td>
      <td><a href="https://www.tandfonline.com/doi/abs/10.2753/JEC1086-4415160105">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>Mediation analysis</td>
      <td>-</td>
      <td>Effect of informational factors</td>
      <td>2013</td>
      <td>Impact of informational factors on online recommendation credibility: The moderating role of source credibility</td>
      <td>DSS</td>
      <td><a href="https://www.sciencedirect.com/science/article/pii/S0167923613001218">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CMA</td>
      <td>NDE, TIE</td>
      <td>-</td>
      <td>Effect of induced change</td>
      <td>2019</td>
      <td>The Identification and Estimation of Direct and Indirect Effects in A/B Tests through Causal Mediation Analysis</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3292500.3330769">Link</a></td>
      <td><a href="https://github.com/xuanyin/causal-mediation-analysis-for-ab-tests?tab=readme-ov-file (R language)">Link</a></td>
    </tr>
    <tr>
      <td>MACR</td>
      <td>TIE</td>
      <td>MF, LightGCN (multi-task)</td>
      <td>Popularity bias</td>
      <td>2021</td>
      <td>Model-Agnostic Counterfactual Reasoning for Eliminating Popularity Bias in Recommender System</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3447548.3467289">Link</a></td>
      <td><a href="https://github.com/weitianxin/MACR">Link</a></td>
    </tr>
    <tr>
      <td>CIRS</td>
      <td>Intervention on the mediator</td>
      <td>PPO</td>
      <td>Filter bubble</td>
      <td>2022</td>
      <td>CIRS: Bursting Filter Bubbles by Counterfactual Interactive Recommender System</td>
      <td>TOIS</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3594871">Link</a></td>
      <td><a href="https://github.com/chongminggao/CIRS-codes">Link</a></td>
    </tr>
    <tr>
      <td>CCF</td>
      <td>Intervention on the mediator, counterfactual data augmentation</td>
      <td>NCF, GRU4Rec, etc.</td>
      <td>Historical bias</td>
      <td>2023</td>
      <td>Causal Collaborative Filtering</td>
      <td>ICTIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3578337.3605122">Link</a></td>
      <td><a href="https://github.com/rutgerswiselab/CCF">Link</a></td>
    </tr>
    <tr>
      <td rowspan="22">Causal Recommendation with Confounder Structure</td>
      <td>-</td>
      <td>Back-door criterion</td>
      <td>MF</td>
      <td>Effect of word- of-mouth recommendation</td>
      <td>2012</td>
      <td>Exploring Social Influence via Posterior Effect of Word-of-Mouth Recommendations</td>
      <td>WSDM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/2124295.2124365">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>Back-door adjustment, instrumental variable</td>
      <td>-</td>
      <td>Effect of recommendations</td>
      <td>2015</td>
      <td>Estimating the Causal Impact of Recommendation Systems from Observational Data</td>
      <td>EC</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/2764468.2764488">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>(causal view)</td>
      <td>MF, etc.</td>
      <td>Feedback loop bias</td>
      <td>2018</td>
      <td>How Algorithmic Confounding in Recommendation Systems Increases Homogeneity and Decreases Utility</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3240323.3240370">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>DEMER</td>
      <td>(causal view)</td>
      <td>DNN(reinforcement learning)</td>
      <td>Unobserved confounding bias</td>
      <td>2019</td>
      <td>Environment Reconstruction with Hidden Confounders for Reinforcement Learning based Recommendation</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3292500.3330933">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CPR</td>
      <td>Intervention on the treatment</td>
      <td>MF,LightGCN, tec.</td>
      <td>Data insufficiency</td>
      <td>2021</td>
      <td>Top-N Recommendation with Counterfactual User Preference Simulation</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482305">Link</a></td>
      <td><a href="https://github.com/ymy4323460/CPR">Link</a></td>
    </tr>
    <tr>
      <td>CauSeR.</td>
      <td>Intervention on the treatment</td>
      <td>SR-GNN</td>
      <td>Popularity bias in session-based RS</td>
      <td>2021</td>
      <td>CauSeR: Causal Session-based Recommendations for Handling Popularity Bias</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482071">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>MCT</td>
      <td>Back-door criterion, CATE</td>
      <td>(self-designed)</td>
      <td>Disability employment</td>
      <td>2021</td>
      <td>Recommending the Most Effective Intervention to Improve Employment for Job Seekers with Disability</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3447548.3467095">Link</a></td>
      <td><a href="https://github.com/trxuanha/maximumcausaltree">Link</a></td>
    </tr>
    <tr>
      <td>DecRS</td>
      <td>Intervention on the treatment</td>
      <td>FM, NFM</td>
      <td>Bias amplification</td>
      <td>2021</td>
      <td>Deconfounded Recommendation for Alleviating Bias Amplification</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3447548.3467249">Link</a></td>
      <td><a href="https://github.com/WenjieWWJ/DecRS">Link</a></td>
    </tr>
    <tr>
      <td>PDA</td>
      <td>Intervention on the treatment</td>
      <td>MF</td>
      <td>Popularity bias</td>
      <td>2021</td>
      <td>Causal Intervention for Leveraging Popularity Bias in Recommendation</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462875">Link</a></td>
      <td><a href="https://github.com/zyang1580/PDA">Official TensorFlow</a>/ <a href="https://github.com/GHxdc/PDA">Reproduced PyTorch</a> </td>
    </tr>
    <tr>
      <td>CR</td>
      <td>Back-door criterion, TIE</td>
      <td>MMGCN(multi-task)</td>
      <td>Clickbait</td>
      <td>2021</td>
      <td>Clicks can be Cheating: Counterfactual Recommendation for Mitigating Clickbait Issue</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462962">Link</a></td>
      <td><a href="https://github.com/WenjieWWJ/Clickbait/">Link</a></td>
    </tr>
    <tr>
      <td>D2Q</td>
      <td>Intervention on the treatment</td>
      <td>(self-designed)</td>
      <td>Duration bias</td>
      <td>2022</td>
      <td>Deconfounding Duration Bias in Watch-time Prediction for Video Recommendation</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539092">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>DeSCoVeR</td>
      <td>Intervention on the treatment</td>
      <td>(self-designed)</td>
      <td>Venue recommendation</td>
      <td>2022</td>
      <td>DeSCoVeR: Debiased Semantic Context Prior for Venue Recommendation</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3477495.3531877">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>IV4Rec</td>
      <td>IV</td>
      <td>DIN, NRHUB</td>
      <td>Recommendation using search data</td>
      <td>2022</td>
      <td>A Model-Agnostic Causal Learning Framework for Recommendation using Search Data</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3485447.3511951">Link</a></td>
      <td><a href="https://github.com/ethan00si/instrumental-variables-for-recommendation">Link</a></td>
    </tr>
    <tr>
      <td>HCR</td>
      <td>Front-door adjustment</td>
      <td>MMGCN</td>
      <td>Unobserved confounding bias</td>
      <td>2022</td>
      <td>Mitigating Hidden Confounding Effects for Causal Recommendation</td>
      <td>TKDE</td>
      <td><a href="https://ieeexplore.ieee.org/abstract/document/10474183/">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>DCR</td>
      <td>Intervention on the treatment</td>
      <td>NFM</td>
      <td>Unobserved confounding bias</td>
      <td>2023</td>
      <td>Addressing Confounding Feature Issue for Causal Recommendation</td>
      <td>TOIS</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3559757">Link</a></td>
      <td><a href="https://github.com/zyang1580/DCR">Link</a></td>
    </tr>
    <tr>
      <td>CaDSI</td>
      <td>Intervention on the treatment</td>
      <td>(self-designed)</td>
      <td>Observed confounding bias</td>
      <td>2023</td>
      <td>Causal Disentanglement for Semantic-Aware Intent Learning in Recommendation</td>
      <td>TKDE</td>
      <td><a href="https://ieeexplore.ieee.org/abstract/document/9736612/">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>DecUCB</td>
      <td>Back-door adjustment</td>
      <td>bandit</td>
      <td>Observed confounding bias</td>
      <td>2023</td>
      <td>User-Regulation Deconfounded Conversational Recommender System with Bandit Feedback</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599539">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>iDCF</td>
      <td>Proxy Variable</td>
      <td>MF</td>
      <td>Unobserved confounding bias</td>
      <td>2023</td>
      <td>Debiasing Recommendation by Learning Identifiable Latent Confounders</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599296">Link</a></td>
      <td><a href="https://github.com/BgmLover/iDCF">Link</a></td>
    </tr>
    <tr>
      <td>CVRDD</td>
      <td>TIE</td>
      <td>MLP(model-agnostic)</td>
      <td>Duration bias</td>
      <td>2023</td>
      <td>Counterfactual Video Recommendation for Duration Debiasing</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599797">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>DML</td>
      <td>Back-door adjustment</td>
      <td>MMoE</td>
      <td>Duration bias</td>
      <td>2023</td>
      <td>Leveraging Watch-time Feedback for Short-Video Recommendations: A Causal Labeling Framework</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3583780.3615483">Link</a></td>
      <td><a href="https://github.com/baiyimeng/DML">Link</a></td>
    </tr>
    <tr>
      <td>CGSR</td>
      <td>Back-door adjustment</td>
      <td>(self-designed)</td>
      <td>Shortcut paths in SBRSs</td>
      <td>2023</td>
      <td>Causality-guided Graph Learning for Session-based Recommendation</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3583780.3614803">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>Back-door adjustment, IPS</td>
      <td>(self-designed, knowledge-based RS)</td>
      <td>Digital agriculture</td>
      <td>2023</td>
      <td>Evaluating Digital Agriculture Recommendations with Causal Inference</td>
      <td>AAAI</td>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/26697">Link</a></td>
      <td><a href="https://github.com/Agri-Hub/AAAI23-Eval-AgriRecommendations">Link</a></td>
    </tr>
  </tbody>
</table>

[Back](#bookmarks-)

## General Counterfactuals-based Methods

<table>
  <thead>
    <tr style="text-align: center;">
      <th>Category / Issue of concern</th>
      <th>Model</th>
      <th>Causal inference method</th>
      <th>Backbone model</th>
      <th>Year</th>
      <th>Title</th>
      <th>Venue</th>
      <th>Paper Link</th>
      <th>Code Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">Domain Adaptation</td>
      <td>-</td>
      <td>ITE</td>
      <td>Linear/regularized kernel methods</td>
      <td>2017</td>
      <td>Predicting Counterfactuals from Large Historical Data and Small Randomized Trials</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3041021.3054190">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>-</td>
      <td>ITE</td>
      <td>Matrix factorization</td>
      <td>2018</td>
      <td>Causal Embeddings for Recommendation</td>
      <td>RecSys</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3240323.3240360">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>Propensity-free DR</td>
      <td>DR</td>
      <td>FFM</td>
      <td>2019</td>
      <td>Improving Ad Click Prediction by Considering Non-displayed Events</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3357384.3358058">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>KDCRec</td>
      <td>ITE</td>
      <td>MF (knowledge distillation)</td>
      <td>2020</td>
      <td>A General Knowledge Distillation Framework for Counterfactual Recommendation via Uniform Data</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3397271.3401083">Link</a></td>
      <td><a href="https://github.com/dgliu/SIGIR20_KDCRec">Link</a></td>
    </tr>
    <tr>
      <td rowspan="5">Data Augmentation</td>
      <td>CF2</td>
      <td>Minimum counterfactuals</td>
      <td>(self-designed)</td>
      <td>2021</td>
      <td>Counterfactual Review-based Recommendation</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482244">Link</a></td>
      <td><a href="https://github.com/CFCF-anonymous/Counterfactual-Review-based-Recommendation">Link</a></td>
    </tr>
    <tr>
      <td>CASR</td>
      <td>Minimum counterfactuals</td>
      <td>NARM, STAMP, SASRec</td>
      <td>2021</td>
      <td>Counterfactual Data-Augmented Sequential Recommendation</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462855">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CauseRec</td>
      <td>Counterfactuals</td>
      <td>(self-designed, sequential recommendation)</td>
      <td>2021</td>
      <td>CauseRec: Counterfactual User Sequence Synthesis for Sequential Recommendation</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462908">Link</a></td>
      <td><a href="https://github.com/LFM-bot/CauseRec">Link</a></td>
    </tr>
    <tr>
      <td>POEM</td>
      <td>Counterfactuals</td>
      <td>GCN</td>
      <td>2022</td>
      <td>Modeling Persuasion Factor of User Decision for Recommendation</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539114">Link</a></td>
      <td><a href="https://github.com/tsinghua-fib-lab/POEM">Link</a></td>
    </tr>
    <tr>
      <td>COCO-SBRS</td>
      <td>Counterfactuals</td>
      <td>(self-designed, sequential recommendation)</td>
      <td>2023</td>
      <td>A Counterfactual Collaborative Session-based Recommender System</td>
      <td>WWW</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3543507.3583321">Link</a></td>
      <td><a href="https://github.com/wzsong17/COCO-SBRS">Link</a></td>
    </tr>
    <tr>
      <td rowspan="4">Fairness</td>
      <td>-</td>
      <td>Counterfactuals</td>
      <td>(self-designed)</td>
      <td>2021</td>
      <td>Towards Personalized Fairness based on Causal Notion</td>
      <td>SIGIR</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3404835.3462966">Link</a></td>
      <td><a href="https://github.com/yunqi-li/Personalized-Counterfactual-Fairness-in-Recommendation">Link</a></td>
    </tr>
    <tr>
      <td>F-UCB</td>
      <td>Counterfactuals</td>
      <td>UCB</td>
      <td>2022</td>
      <td>Achieving Counterfactual Fairness for Causal Bandit</td>
      <td>AAAI</td>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/20653">Link</a></td>
      <td>-</td>
    </tr>
    <tr>
      <td>CLOVER</td>
      <td>Counterfactuals</td>
      <td>MELU</td>
      <td>2022</td>
      <td>Comprehensive Fair Meta-learned Recommender System</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3534678.3539269">Link</a></td>
      <td><a href="https://github.com/weitianxin/CLOVER">Link</a></td>
    </tr>
    <tr>
      <td>PSF-RS</td>
      <td>Minimum counterfactuals</td>
      <td>(self-designed)</td>
      <td>2023</td>
      <td>Path-Specific Counterfactual Fairness for Recommender Systems</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599462">Link</a></td>
      <td><a href="https://github.com/yaochenzhu/PSF-VAE">Link</a></td>
    </tr>
    <tr>
      <td rowspan="3">Explanation</td>
      <td>PRINCE</td>
      <td>Minimum counterfactuals</td>
      <td>HIN</td>
      <td>2020</td>
      <td>PRINCE: Provider-side Interpretability with Counterfactual Explanations in Recommender Systems</td>
      <td>WSDM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3336191.3371824">Link</a></td>
      <td><a href="https://github.com/azinmatin/prince">Link</a></td>
    </tr>
    <tr>
      <td>CountER</td>
      <td>Minimum counterfactuals</td>
      <td>MLP(model-agnostic, black-box)</td>
      <td>2021</td>
      <td>Counterfactual Explainable Recommendation</td>
      <td>CIKM</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3459637.3482420">Link</a></td>
      <td><a href="https://github.com/chrisjtan/counter">Link</a></td>
    </tr>
    <tr>
      <td>CounterNet</td>
      <td>Minimum counterfactuals</td>
      <td>(self-designed)</td>
      <td>2023</td>
      <td>CounterNet: End-to-End Training of Prediction Aware Counterfactual Explanations</td>
      <td>KDD</td>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3580305.3599290">Link</a></td>
      <td><a href="https://github.com/BirkhoffG/counternet">Link</a></td>
    </tr>
  </tbody>
</table>

[Back](#bookmarks-)

## License

This project is licensed under the MIT License.
