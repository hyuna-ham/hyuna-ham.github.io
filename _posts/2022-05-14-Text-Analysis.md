---
layout: post
title: Text analysis 
subtitle: Tone in financial disclosures
cover-img: /assets/img/language.png
thumbnail-img: /assets/img/sentiment.png
share-img: /assets/img/sentiment.png
---

<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax:
		{inlineMath: [['$','$'], ['\\(','\\)']],
		 displayMath: [ ['$$','$$'], ["\\[","\\]"] ], 
            	 processEscapes: true }
		 });
</script>
<script src="//cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

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
This study analyzes stocks listed on the New York Stock Exchange, the American Stock Exchange, and the National Association of Securities Dealers Automated Quotations. The daily rates of return and financial indicators of individual companies and reported data will be collected from Bloomberg. Addtionally, it will collect annual and quarterly filings, financial analyst reports, and the earnings conference call transcripts of individual companies from the SEC’s EDGAR website, Thomson Investext database, and SeekingAlpha website. Furthermore, FinBERT (Huang, Wang, and Yang, 2022) will be used for sentiment analysis, which is trained with 2.5B tokens of corporate reports 10-K and 10-Q; 1.3B tokens of earnings call transcripts; and 1.1B tokens of analyst reports with 10,000 sentences labeled as positive, neutral, and negative. The results will be grouped according to announcement dates and fiscal quarters. 

**2.2 Hypotheses and Methodology** <br>

_Hypothesis 1: Better (worse) financial indicators will lead to a positive (negative) financial report tone._

Narratives of financial reports provide investors withare for investors to a better understanding of the understand financial indicators. Thus, in a normal situationssituations, tones of financial indicators and the financial report tone should be in have a positive relationship. To discover the relationship between financial indicators and sentiment scores, the following analysis was conducted:

$$ FI_{j} = \alpha_{Senti} + \beta_{Senti} \cdot Senti + ε, $$

where $FI_{j}$ is a financial indicator $j$ in return on equity, current ratio, sales growth, debt-to-equity ratio, and asset turnover; $Senti$ is the sentiment score of the corporate reports from FinBERT; and $ε$ denotes the error term.

_Hypothesis 2: Larger differences from previous public announcements result in louder investor responses, even when controlling for changes in financial indicators._

According to De Bondt and Thaler (1985), people tend to overreact to “unexpected and dramatic news.” Consequently, investors may respond louder when public announcement tones show a larger difference between the current sentiment and the previous scores of previous public announcements. Therefore, the relationship between the differences in the tone of public announcements and market responses is analyzed as follows:

$$ CAV[0,3] = \alpha_{SentiDiff}+\beta_{SentiDiff} \cdot SentiDiff + \sumγ \cdot Controls_{v} + ε, $$

where $CAV[0,3]$ represents the cumulative abnormal volume for three days, starting from the reporting date; $SentiDiff$ is the difference between the current sentiment and previous scores; and $Controls_{v}$ includes all the control variables considered in Bochkay, Hales, and Chava (2020). <br>

### References
Abrahamson, E., & Amir, E. (1996). The information content of the president's letter to shareholders. _Journal of Business Finance and Accounting_, 23, 1157-1182.

Bochkay, K., Brown, S. V., Leone, A. J., & Tucker, J. W. (2022). Textual analysis in accounting: What’s Next? _Working Paper_.

Bochkay, K., Hales, J., & Chava, S. (2020). Hyperbole or reality? Investor response to extreme language in earnings conference calls. _Accounting Review_, 95 (2), 31-60.

Brown, N. C., Crowley, R. M., & Elliott, W. B. (2020). What are you saying? Using topic to detect financial misreporting. _Journal of Accounting Research_, 58 (1), 237-291.

De Bondt, W. F., & Thaler, R. (1985). Does the stock market overreact? _Journal of finance_, 40 (3), 793-805.

Devlin, J., Chang, M. W., Lee, K., & Toutanova, K. (2018). Bert: Pre-training of deep bidirectional transformers for language understanding. _arXiv:1810.04805_.

Feldman, R., Govindaraj, S., Livnat, J., & Segal, B. (2010). Management’s tone change, post earnings announcement drift and accruals. _Review of Accounting Studies_, 15 (4), 915-953.

Hartmann, J., Heitmann, M., Siebert, C., & Schamp, C. (2022). More than a Feeling: Accuracy and Application of Sentiment Analysis. _International Journal of Research in Marketing_.

Henry, E. (2008). Are investors influenced by how earnings press releases are written? _Journal of Business Communication_, 45 (4), 363-407.

Huang, A., Wang, H., & Yang, Y. (2022). FinBERT—A Large Language Model Approach to Extracting Information from Financial Text. _Working Paper_.

Ingram, R. W., & Frazier, K. B. (1983). Narrative disclosures in annual reports. _Journal of Business Research_, 11 (1), 49-60.

Kothari, S. P., Li, X., & Short, J. E. (2009). The effect of disclosures by management, analysts, and business press on cost of capital, return volatility, and analyst forecasts: A study using content analysis. _Accounting Review_, 84 (5), 1639-1670.

Li, F. (2010). The information content of forward‐looking statements in corporate filings—A naïve Bayesian machine learning approach. _Journal of Accounting Research_, 48 (5), 1049-1102.

Martinc, M., Pollak, S., & Robnik-Šikonja, M. (2021). Supervised and unsupervised neural approaches to text readability. _Computational Linguistics_, 47 (1), 141-179. <br>

<br>
### 2. Appendix 1: BERT and Others <br>

Bidirectional encoder representations from transformers (BERT) is a pre-trained transfer learning model based on an natural language processing (NLP) model, Transformer (Devlin, Chang, Lee, and Toutanova, 2018). It learns large amounts of objective-free data in an unsupervised pretraining manner and uses them suitably with additional fine-tuning. The following explains BERT’s pre-training process.

To solve the out-of-vocabulary issue, BERT uses WordPiece embedding (WPE). As transformed from byte-pair encoding (BPE), WPE segregates every word by character. While BPE merges the most frequently appearing pairs of letters into one letter, WPE merges pairs of letters that maximize the likelihood of the corpus. That is, it is judged that the characters have a higher probability of becoming a unit, when the higher the frequency of the two characters appearing together than when the two characters appear separately, the higher the probability of becoming a unit. This merging leads to a meaningful separation of subwords, allowing efficient handling of new words. The model then matches information regarding the sentence to each word through segment embedding and combines the location information through positional embedding.

BERT uses a masked language model (MLM) and next sentence prediction (NSP) for pretraining. The MLM masks 15% of the entire word piece randomly and learns to guess a word hidden by surrounding words. As a result, Devlin et al. (2018) insisted that contextual information is better learned through MLM than through a left-to-right language model, which words are only predicted from previous words. Moreover, the relationship between two sentences was analyzed using the NSP process, which forecasts the connectivity of two sentences. Specifically, model learning is afoot with the “IsNext” label on 50% connected sentences and the “NotNext” label on 50% randomized sentences.

Consequently, a pretrained model was used with additional learning targeted for the purpose. BERT is an epoch-making event that shows the best performance with numerous NLP works. The enormous amount of data used for training the model can be referred to as one reason. BERT was pre-trained with BooksCorpus (800M words) and English Wikipedia (2,500M words). With fine-tuning, users can simply use a pretrained model to serve their taste.

After BERT, developments of NLP models have accelerated, such as generative pre-training (GPT) 3 armed with more learning data or robust optimized BERT (RoBERTa) equipped with improved learning performance. Some were alleged to edge out BERT. Thus, it would be meaningful if other models were additionally learned with financial data and compared with FinBERT. Moreover, currently, FinBERT classifies positive, neutral, and negative results into -1, 0, and 1, respectively. In this regard, improving the model in a manner that reflects how positive, neutral, and negative results are achieved will be another task worth trying.

### Appendix 2: Other Applications of NLP in Accounting <br>

NLP models can be used for sentiment analysis and various research topics of text analysis in accounting. For example, the readability of financial reports can be scored by using the models as it can predict the words contained in the reports, such as in Martinc, Pollak, and Robnik-Šikonja (2021). Additionally, using topic discovery models that “summarize a document by grouping words into themes,” we can distinguish different types of competition or detect financial misreporting (Brown, Crowley, and Elliott, 2020).
