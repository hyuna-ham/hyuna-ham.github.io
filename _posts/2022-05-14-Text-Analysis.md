---
layout: post
title: The Tone of Financial Disclosures
subtitle: Characteristics of extended hour trading returns when intraday returns increase
cover-img: /assets/img/chart.jpg
thumbnail-img: /assets/img/sentiment.png
share-img: /assets/img/hxblock.png
---

### 1. Introduction <br>

**1.1 Literature Review** <br>
Accounting has long been committed to discerning the emotions involved in text data. In 1983, Ingram and Frazier (1983) analyze the relationship between the narrative data of accounting reports and corporate performance. Related research has been actively conducted on the importance of the sentiment analysis of various narrative data, including accounting reports, CEO letters to shareholders, news, and audit reports. For example, Abrahamson and Amir (1996) study the relationship between negative words in a president’s letter to shareholders and the future rate of return. Henry (2008) explores investors’ responses to different tones of earnings press releases. Kothari, Li, and Short (2009) find that positive disclosures lead to weakened corporate risk, such as a high cost of capital, stock return volatility, and analyst forecast dispersion. Feldman, Govindaraj, Livnat, and Segal (2010) navigated the links between changes in management’s tone at MD&A sections and market responses. Moreover, Bochkay, Hales, and Chava (2020) highlighted that managers’ extreme wording during earnings conference calls results in an increase in trading volumes and rising stock prices.


**1.2 Contribution** <br>
I investigate the nonlinear relationship between extended hour trading and intraday returns using a deep learning model with an attention method, which has recently attracted attention. This study contributes to elaborately illuminates the underlying dynamics of the financial market. Furthermore, I propose HxNet to determine the characteristics of historical data of the extended hour trading sessions that are important for predicting future intraday returns. This model can be used for intraday stock price data and stock data on various frequency levels. Moreover, the model can be applied to diverse time-series data, beyond stock prices. Furthermore, this study provides a guide for the use of machine learning in finance. This model may not be a mere tool to increase the prediction rate, but a method to better understand the financial market by identifying the relationship between the nonlinear pattern of the past and future returns. <br><br>

### 2.	Methodology <br>

**2.1 Data** <br>
I collect data on stocks listed in the New York Stock Exchange (NYSE), American Stock Exchange (AMEX), and Nasdaq National Market System (NMS) at least once since 2010 from the NYSE Trade and Quote (TAQ) database. 

**2.2 Model** <br>
As demonstrated below, we will design a model to learn the nonlinear relationship between extended hour trading and intraday returns and find the significance of variables in the intraday return direction by adding attention to a deep learning structure. This model uses convolution layers that have the advantage of capturing features and adds an attention module for easy interpretation of results (which can be developed through experiments). I construct an attention structure as a module that has scalability to add it anywhere between neural network layers. This model is compared to existing models, such as regression and Convolutional Neural Networks, to evaluate its performance and determine the important features of the time-series for predicting future daytime trading session returns through attention weight.

![hxblock](/assets/img/intext_hxblock.PNG) <br>


### Appendix: Easy explanation on the concept of attention <br>
Attention is a machine-learning method that mimics human attention and refers to crucial input parts. The methods used for attention have been extensive. You may refer to the photos below by Xu et al. (2015) for an in-depth understanding. The images show that the focus is placed on shapes corresponding to the underlined words. Thus, attention is a method of letting a model concentrate on and refer to parts that are crucial for prediction.

![xu2015](/assets/img/xu2015.png)

The decoder refers to the entire input sentence in the encoder at every time step when predicting the output. Bahdanau et al. (2014) develop a model to learn efficiently by focusing more related words on the word to be predicted at that point among the words in the encoder, rather than referring to the entire input sentence with the same importance. They suggest the following process. First, when the input is fed into the decoder, the attention score is calculated from the current hidden states of the encoder (there are various methods such as dot-product attention). Then, the score is normalized to 1 via softmax and a weighted sum is obtained by multiplying it to the hidden state of the encoder. The result of the attention value is called a context vector because it contains an encoder context. Attention is linked to the current hidden state of the decoder, so that we can evaluate the important features (words) for the prediction. <br><br>

### References
Akbas, F., Boehmer, E., Jiang, C., & Koch, P.D., 2022. Overnight returns, daytime reversals, and future stock returns. _Journal of Financial Economics_ 145, 850-875.

Berkman, H., Koch, P.D., Tuttle, L., & Zhang, Y.J., 2012. Paying attention: Overnight returns and the hidden cost of buying at the open. _Journal of Financial and Quantitative Analysis_ 47, 715-741.

Cox, D.R., & Peterson, D.R., 1994. Stock returns following large one‐day declines: Evidence on short‐term reversals and longer‐term performance. _Journal of Finance_ 49, 255-267.

Ferreira, F.G.D.C., Gandomi, A.H., & Cardoso, R.T.N., 2021. Artificial intelligence applied to stock market trading: A review. _IEEE Access_ 9, 30898-30917.

Ham, H., Ryu, D., & Webb, R.I., 2022. The effects of overnight events on daytime trading sessions. _International Review of Financial Analysis_ 83, 102228.

Levi, S., Livnat, J., Zhang, L., & Zhang, X.-J., 2018. Is extended-hours trading indicative of subsequent returns? _Journal of Investing_ 27, 9-19.

Lou, D., Polk, C., & Skouras, S., 2019. A tug of war: Overnight versus intraday expected returns. _Journal of Financial Economics_ 134, 192-213.

Obthong, M., Tantisantiwong, N., Jeamwatthanachai, W., & Wills, G., 2020. A survey on machine learning for stock price prediction: Algorithms and techniques. 2nd International Conference on Finance, Economics, _Management and IT Business_, 63-71.

Park, J., 1995. A market microstructure explanation for predictable variations in stock returns following large price changes. _Journal of Financial and Quantitative Analysis_ 30, 241-256.

Xu, K., Ba, J., Kiros, R., Cho, K., Courville, A., Salakhudinov, R., Zemel, R., & Bengio, Y., 2015. Show, attend and tell: Neural image caption generation with visual attention. _Proceedings of the 32nd International Conference on Machine Learning_, 2048-2057.
