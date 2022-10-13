---
layout: post
title: Text Analysis 
subtitle: Tone in Financial Disclosures
cover-img: /assets/img/language.png
thumbnail-img: /assets/img/sentiment.png
share-img: /assets/img/sentiment.png
---

### 1. Introduction <br>

**1.1 Literature Review** <br>
Accounting has long been committed to discerning the emotions involved in text data. In 1983, Ingram and Frazier (1983) analyze the relationship between the narrative data of accounting reports and corporate performance. Related research has been actively conducted on the importance of the sentiment analysis of various narrative data, including accounting reports, CEO letters to shareholders, news, and audit reports. For example, Abrahamson and Amir (1996) study the relationship between negative words in a president’s letter to shareholders and the future rate of return. Henry (2008) explores investors’ responses to different tones of earnings press releases. Kothari, Li, and Short (2009) find that positive disclosures lead to weakened corporate risk, such as a high cost of capital, stock return volatility, and analyst forecast dispersion. Feldman, Govindaraj, Livnat, and Segal (2010) navigated the links between changes in management’s tone at MD&A sections and market responses. Moreover, Bochkay, Hales, and Chava (2020) highlighted that managers’ extreme wording during earnings conference calls results in an increase in trading volumes and rising stock prices.

Thus, sentiment analysis techniques help better understand the information related to investment and credit decisions and corporate stakeholders make rational decisions. The dictionary method, as a classic sentiment analysis method, uses lists of words that accompany the emotions involved in each word. In general, the frequencies of positive and negative words were counted first. Then, the sentiment of the documents is calculated from the difference between the number of positive and negative words scaled by the total number of words in the documents. As a simple method, the dictionary method helps avoid the researcher’s subjectivity and identifies which individual words contribute to the entire sentiment score. Despite its simplicity and usability, the dictionary method has unequivocal limits in that it does not consider the context of words.

Li (2010) asserted that the dictionary method does not work well for analyzing corporate financial statements. He trailblazed machine learning-based sentiment analysis by evaluating financial disclosures through statistical learning methodology. Since then, sentiment analysis has been conducted with multifaceted machine learning models, from conventional naive Bayesian, support vector machine, and random forest models to convolutional neural network, long short-term memory, and bidirectional encoder representations from transformers (BERT) models. Unlike the dictionary method, the machine-learning method takes the context into consideration. According to Hartmann, Heitmann, Siebert, and Schamp (2022), the accuracy of sentiment analysis increases from 73.49% in the dictionary method to 82.62% in traditional machine learning methods. When switching to deep learning, the accuracy increased to 87.18%. Nonetheless, 97.4% of the papers on sentiment analysis published in the top accounting journals still use the dictionary method; however, studies utilizing deep learning-based sentiment analysis have rarely been conducted (Bochkay, Brown, Leone, and Tucker, 2022).

Google announced the development of BERT (Devlin, Chang, Lee, and Toutanova, 2018), a pre-trained model for natural language processing (NLP), in 2018. BERT attracted attention because it produced the best performance in various types of NLP. However, it has demonstrated limits in adopting professional languages, as the characteristics of individual languages vary. Therefore, the recent development of FinBERT by Huang, Wang, and Yang (2022) has drawn attention. They used BERT to learn about financial reports, analyst reports, and earnings conference call transcripts to address this problem. They showed that FinBERT outperformed BERT in the financial domain.

**1.2 Contribution** <br>
This study unveils the relationship between financial indicators and narrative data tones by utilizing the latest deep learning-based sentiment analysis technology, FinBERT. It also provides a more accurate corporate analysis using deep-learning-based sentiment analysis. It ultimately aims to help corporate stakeholders, including investors, make decisions more rationally. It also checks whether corporate narrative explanations are properly addressed to determine corporate financial status in the eyes of management. For this purpose, the tones of financial indicators and financial reports are compared. Moreover, this study analyzes the impact of these documents on the market by examining the responses of the stock market brought about by differences in public announcements. It serves as an opportunity to gauge whether current public announcement regulations perform well. <br><br>

### 2. Data and Methodology <br>

**2.1 Data** <br>
We analyzed stocks listed on the New York Stock Exchange, the American Stock Exchange, and the National Association of Securities Dealers Automated Quotations. We gathered the daily rates of return and financial indicators of individual companies and reported data published in Bloomberg. We collected annual and quarterly filings, financial analyst reports, and the earnings conference call transcripts of individual companies from the SEC’s EDGAR website, Thomson Investext database, and SeekingAlpha website. In addition, we harnessed FinBERT from Huang, Wang, and Yang (2022) for sentiment analysis. FinBERT is trained with 2.5B tokens of corporate reports 10-K and 10-Q; 1.3B tokens of earnings call transcripts; and 1.1B tokens of analyst reports with 10,000 sentences labeled as positive, neutral, and negative.

We conducted a sentiment analysis of disclosure documents using FinBERT. The results are grouped according to announcement dates and fiscal quarters. Using the results from FinBERT, we verify the proposed hypotheses.

**2.2 Methodology** <br>
To discover the relationship between financial indicators and sentiment scores, the following analysis was conducted:

$$ FI_{j} = \alpha_{senti} + \beta_{senti} \cdot Senti + ε$$

where $FI_{j}$ is a financial indicator _j_ in return on equity, current ratio, sales growth, debt-to-equity ratio, and asset turnover; _Senti_ is the sentiment score of the corporate reports from FinBERT; and _ε_ denotes the error term.


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
