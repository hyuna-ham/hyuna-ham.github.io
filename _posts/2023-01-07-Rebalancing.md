---
layout: post
title: Rebalancing 
subtitle: Optimal rebalancing using deep reinforcement learning
cover-img: /assets/img/rebalance.jpg
thumbnail-img: /assets/img/rebalancing.jpg
share-img: /assets/img/rebalancing.jpg
---

Mean-variance optimization (MVO) (Markowitz and Todd, 2000) is a representative model for creating an optimal target portfolio by maximizing the return/risk ratio. In this optimization process, MVO considers individual risk preferences. However, once investors derive their optimal target portfolio, maintaining the balance between assets is a non-trivial task. Managers need active portfolio rebalancing considering the expected returns of the asset classes in the portfolio and the changing nature of the risk profile. One of the major factors that influences the rebalancing decision is transaction costs, including commissions, market impact, personnel costs, and technological resources. If transaction costs are greater than the expected return of the rebalanced portfolio, then no adjustment should be undertaken.

Conventional rebalancing methods include periodic rebalancing (Donohue and Yip, 2003), where rebalancing is performed once every month or quarter, and tolerance band rebalancing (Masters, 2003), where a threshold, called a tolerance band, is set and rebalancing is conducted if any asset class hits the threshold. The strength of periodic rebalancing is its easy application, although it fails to consider market behavior in its trading decisions. In this respect, tolerance band rebalancing can be a good alternative because it follows market movements. However, this is restricted to a fixed band, and setting the right tolerance band for every asset in a portfolio is a challenging task.

Sun et al. (2006) proposed three distinct cost functions and optimized them using dynamic programming (DP). This study proposes an insightful objective function for the optimal rebalancing problem. Since portfolio optimization aims to maximize a utility function, the utility gap between the optimal and current portfolios is set as a tracking error. Hence, the goal is to minimize this gap. The authors also consider the transaction costs incurred to buy and sell assets to achieve the rebalancing. The results confirm the higher performance and robustness of the proposed model compared with traditional rebalancing models.

DP is a great tool for sequential decision-making problems. However, it suffers from the curse of dimensionality. For instance, as the number of asset classes increases, the computational complexity of DP increases exponentially. Additionally, in the modeling process, DP assumes that we know the market environment. The Markov decision process (MDP) assumes that we know the reward and state transition probability. As the market environment where we aim to accomplish the optimal rebalancing is unpredictable, Sun et al. (2006) added a Gaussian noise term to every new state reached through the previous action and its reward. This process provides a probabilistic uncertainty model to explain the market environment. The fundamental reason for applying random Gaussian noise in the modeling process is that DP is a calculation algorithm, not a learning algorithm such as in deep learning models. Presumably, there is a disconnect between market modeling using random noise and the real stock market. Better scenarios would avoid direct market modeling, instead learning it from its informative data.

By contrast, deep reinforcement learning (DRL) is free from DP’s problems. For optimal rebalancing, DRL interacts with the market environment through data and learns from it. As DRL is a data-based learning algorithm, it neither requires environment modeling nor is it ruled by the curse of dimensionality. The model can predict expected rewards from the new state reached by current actions.

Recent studies on DRL applied in the domain of the rebalancing problem include Lim, Cao, and Quek (2022), who used Q-learning combined with deep learning models. Q-learning has a performance-lowering problem because the correlation between the data and learning is unstable since the target value can change drastically (Mnih et al., 2013). Moreover, Lim, Cao, and Quek’s (2022) model merely considers portfolio weights; it does not reflect rebalancing trading costs, which are a major factor that influences rebalancing decisions.

Therefore, this study suggests the soft actor-critic (SAC) model (Haarnoja et al., 2018) for the optimal rebalancing problem. This model can not only overcome the performance-lowering problem because of the data correlation and radical target value changes, it also learns suboptimal information, which provides extra model robustness in a dynamic environment. As a DRL model, SAC has all the advantages of DRL; hence, it serves as a great alternative to the DP model. Furthermore, considering that optimal rebalancing occurs in a dynamically changing stock market, its robustness achieved by learning optimal and suboptimal conditions adds strength in solving this problem. <br>



### References
Bellman, R (1952). On the theory of dynamic programming. _Proceedings of the National Academy of Sciences_, 38, 716-719. https://doi.org/10.1073/pnas.38.8.716 

Busoniu, L., Babuska, R., De Schutter, B., & Ernst, D. (2017). Reinforcement Learning and Dynamic Programming using Function Approximators. CRC Press, Boca Raton, Florida. https://doi.org/10.1201/9781439821091

Donohue, C., & Yip, K. (2003). Optimal portfolio rebalancing with transaction costs. _Journal of Portfolio Management_, 29, 49-63. https://doi.org/10.3905/jpm.2003.319894 

Haarnoja, T., Zhou, A., Hartikainen, K., Tucker., G., Ha., S., Tan, J., Kumar, V., Zhu, H., Gupta, A., Abbeel, P., & Levine, S. (2018). Soft actor-critic algorithms and applications. _arXiv preprint_ arXiv:1812.05905

Lim, Q.U.E., Cao, Q., & Quek, C (2022). Dynamic portfolio rebalancing through reinforcement learning. _Neural Computing and Applications_, 34, 7125-7139. https://doi.org/10.1007/s00521-021-06853-3 

Luce , R.D. (2000). Utility of Gains and Losses: Measurement-theoretical and Experimental Approaches. Lawrence Erlbaum Associates, Mahwah, New Jersey.

Markowitz, H.M., & Todd, G.P. (2000). Mean-variance Analysis in Portfolio Choice and Capital Markets. _John Wiley & Sons_, Hoboken, New Jersey.

Masters, S.J. (2003). Rebalancing. _Journal of Portfolio Management_, 29, 52-57. https://doi.org/10.3905/jpm.2003.319883 

Mnih, V., Koray, K., Silver, D., Graves, A., Antonoglou, I., Wierstra, D., & Riedmiller, M. (2013). Playing atari with deep reinforcement learning. _arXiv preprint_ arXiv:1312.5602.

Sun, W., Fan, A., Chen, L., Schouwenaars, T., Albota, M. (2006). Optimal rebalancing for institutional portfolios. _Journal of Portfolio Management_, 32, 33-43. https://doi.org/10.3905/jpm.2006.611801 

Tang, H., & Haarnoja, T. (2017). Learning diverse skills via maximum entropy deep reinforcement learning. https://bair.berkeley.edu/blog/2017/10/06/soft-q-learning

White III, C.C., White, D.J. (1989). Markov decision processes. _European Journal of Operational Research_, 39, 1-16. https://doi.org/10.1016/0377-2217(89)90348-2
