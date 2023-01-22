---
layout: post
title: Robo-Advisors 
subtitle: What's next?
cover-img: /assets/img/ai.jpeg
thumbnail-img: /assets/img/robo.jpg
share-img: /assets/img/esg.jpg
---

### 1. Introduction <br>

The finance industry continues to adopt new technologies to provide financial services more economically and efficiently. One service that achieves this is the robo-advisor. Robo-advisors are digital platforms that help small investors receive simple and accessible asset management services for financial planning using automated algorithms. For example, Bank of America requires $25,000 to open an account with a personal financial advisor but only $5,000 with a robo-advisor. Additionally, robo-advisors provide financial advice at a much lower cost compared to traditional advisory services. For example, a fully automated robo-advisor charges a fee of up to 0.25% of managed assets, while a traditional human-advisor fee is more than 0.75% and may reach 1.5% (Lopez, Babcic and De La Ossa, 2015). Because of these advantages, the robo-advisor market is steadily expanding as shown in Figure 1. The industry is still in the early growth stages but has enormous potential.

**Figure 1: Market Growth Trend of Robo-Advisor** <br>
_Note_: Shows the assets under management (AUM) of the robo-advisor provided by Statista. The AUM of the robo-advisor industry in 2022 is projected to be $1.66 trillion. The AUM is estimated to grow at an annual rate of 14.19% and to reach $3.22 trillion in 2027.
![Figure1](/assets/img/robo-fig1.PNG) <br>

Robo-advisor services are composed of several processes, as shown in Figure 2. Academic studies should be conducted in each of those fields to promote and guide the development of the automated processes offered. This report organizes robo-advisor processes into six categories. Within each category the current problems are examined and future directions suggested. 

**Figure 2: Processes of a Robo-Advisor**
![Figure2](/assets/img/robo-fig2.png) <br>

<br>
### 2. Individual Risk Tolerance <br>

Foerster, Linnainmaa, Melze and Previtero (2017) showed that financial advisors exert considerable influence over customers’ asset allocations but have limitations in providing customized services. As personalization is key for robo-advisors, understanding individual risk tolerance is essential.

Risk tolerance is the maximum degree of uncertainty that an individual is willing to accept when making financial decisions (Grable, 2008). It is a critical factor for individual customers when making various financial decisions as well as a key intrinsic variable in financial planning, investment suitability analysis, and customer decision-making structures. Financial risk tolerance greatly influences both short- and long-term financial decisions, such as purchasing decisions and saving for retirement. However, robo-advisors identify the risk tolerance of investors through one-size-fits-all questionnaires, which are too simple and do not always provide a comprehensive overview of a client’s financial situation and characteristics. Hence, they are limited in understanding the customers’ tendencies.

Noting its importance, economists have long conducted studies to understand individual risk tolerance (Latané, 1960; Cohn, Lease, and Schlarbaum, 1975). For example, Faig and Shum (2002) found that customers' individual projects, such as starting businesses or purchasing houses, influence their individual investment portfolio choices. Filbeck, Hatfield and Horvath (2005) analyzed the relationship between an investor’s personality and their risk tolerance. Additionally, Kumar, Page and Spalt (2011) showed that religious beliefs can influence individual investment portfolio choices.

Additionally, poor health can affect various factors that may impact portfolio composition, including the utility of consumption, risk aversion, and labor returns (Rosen and Wu, 2004). Hence, health status is also an important factor in understanding individual risk tolerance. Despite this importance, research on the effects of an individual's health status on their independent risk tolerance has only relatively recently begun to draw attention. For example, Addoum, Korniotis and Kumar (2017) revealed that height and obesity influence the portfolio choices of investors, and Døskeland and Kvaerner (2022) showed that a history of cancer diagnosis increases risk aversion.

In this regard, future research challenges relate to individual health and risk tolerance. For example, there might be an association between risk tolerance and environmental diseases, such as rhinitis, asthma, and atopy, the prevalence of which has been rapidly increasing recently due to climate change and environmental change. Patients with environmental diseases are more sensitive to the weather; Bassi, Colacito and Fulghieri (2013) showed that weather affects individual risk tolerance. In addition, since these diseases are chronic and require funds for continuous treatment and management, a significant relationship may exist between investment style and the presence or absence of disease. As such, efforts are required to study individual risk tolerance from more varied perspectives.

<br>
### 3. Portfolio <br>

Portfolio optimization, such as modern portfolio theory (MPT) and Black-Litterman (BL), is a representative methodology for portfolio construction (Markowitz, 1952; Black and Litterman, 1990). Many robo-advisor companies structure their portfolios according to this methodology. For instance, Wealthfront, one of the largest robo-advisor companies, uses the MPT, while Betterment uses the BL model. Arguably, portfolio optimization provides the most intuitive method of finding the best portfolio to maximize return on risk. However, the model is highly sensitive to input values, that is, covariance matrix and expected future return. Moreover, the input itself is difficult to know (Michaud, 1989; Best and Grauer, 1991; Chopra and Ziemba, 2013). Therefore, if no constraints or additional solutions are applied, portfolio diversification effects cannot be expected because the weight is concentrated in a small number of stocks. Although many studies have sought to identify and solve the problems of the portfolio optimization method (Britten-Jones, 1999; Jagannathan and Ma, 2003; Ledoit and Wolf, 2003; Ban, El Karoui and Lim, 2018), they only mitigate the aforementioned problems to a limited degree; the fundamental problems remain unresolved. 

Recently, a new investment philosophy called goal-based investing (GBI) has begun gaining popularity with the emergence of automated investment systems and customized services. GBI is a personal goal-oriented investment strategy that differs from conventional strategies that focus only on market behavior (Sironi, 2016). It places individuals at the center of the investment decision-making process and considers the real risk faced by individuals to be not market volatility but the probability of falling short of individual goals (Sironi, 2016). Traditional investments aim to maximize expected returns, while GBI aims to maximize the probability of achieving individual goals. The GBI philosophy thus fits well with robo-advisor service offerings, which focus on personalization. Though attempts are being made to introduce GBI into practice, it is in the early stages, and research on GBI remains scarce. Therefore, studies on an appropriate methodology for GBI are needed.

<br>
### 4. Rebalancing <br>

Over time, the value of assets may change according to market performance. Therefore, without rebalancing, a portfolio may no longer match the acceptable range of risk over time, even if the initial composition is optimal. It may seem harmless to allocate more shares than initially planned when stock prices rise. However, no market rally lasts forever, and if the trend changes, the portfolio will become overexposed during a decline. Therefore, after setting the target portfolio, the assets should be rebalanced. While the power of rebalancing to improve returns and reduce risks is generally recognized, relatively little research has focused on the best way to implement rebalancing policies (Sun, Fan, Chen, Schouwenaars and Albota, 2006; Masters, 2013; Kimball, Shapiro, Shumway and Zhang, 2020). 

<br>
### 5. Market Microstructure and Optimal Execution <br>

Of late, research has been increasingly focusing on the market microstructure, where potential investor demand is ultimately reflected in the form of transactions (Madhavan, 2000).

Understanding market microstructure is essential for executing orders, especially in large volumes. Large buy orders can unexpectedly raise market prices, resulting in more expensive purchases. As such, transactions affect market prices (i.e., price impact), and this can greatly influence investment returns (Tsoukalas, Wang and Giesecke, 2019). 

However, managing the price impact is challenging because it requires a model for the individual transactions of each market participant. Large technology development and human resource expenditure are also required. Nevertheless, technological advances and high-frequency trading are areas that require continuous research because they rapidly alter the market microstructure (O'Hara, 2015).

<br>
### 6. Human-Computer Interaction (HCI) <br>

In the service industry, interaction with customers is essential for businesses to feel the pulse of their customers and suitably serve them, which will lead to increased profitability. According to Calmon, Ciocan and Romero (2021), customers’ goodwill toward a platform is dynamic and can change depending on the quality of their past interactions, which is closely related to the service's revenue. Additionally, Hathaway, Emadi and Deshpande (2022) stated that, to improve revenue and customer service, the company must provide personalized services based on customer records. They argued that inquiries or complaints can be prevented at an individual level through such services.

Personalized customer interaction is also a key area for robo-advisors. A robo-advisor should serve not only as an advisor but also make automated investment decisions. Therefore, interacting with clients digitally is central to robo-advisor services. Capponi, Olafsson and Zariphopoulou (2022) showed that the success of a robo-advisor service depends highly on its ability to provide personalized financial services. To achieve this, they suggested that information from customers should be properly received and used for communication.

Therefore, research evaluating whether robo-advisors sufficiently play the advisor role through personalized customer interactions is first needed, starting with the design of robo-advisor apps. 

<br>
### 7. Corporates and Financial Markets <br>

Understanding corporates and financial markets is important for making wise investment decisions, prompting numerous studies to analyze companies and financial markets from various perspectives.

Recently, machine learning (ML) has been used in many fields, and finance is no exception. Gu, Kelly and Xiu (2020) used ML in measuring equal risk premiums and showed that their model achieved more than double the performance of the traditional regression-based strategies. They argued that ML methods can be used to easily apply variable selection and dimension reduction to the high-dimensional data of various kinds of predictors, prevent overfitting through regularization, and apply complex and non-linear models. 

The concept of “attention” in deep learning is being increasingly recognized as a factor contributing to excellent performance. Most importantly, however, its explanatory power is remarkable. Through the attention technique, it is easier to explain the features that are important for prediction. This complements the limitations of deep learning models, which are a black box despite their excellent performance. As a result, beyond solely being a means to increase predictability, attention helps in understanding the relationship between the non-linear patterns of past returns and future returns and can be used to establish and develop a financial economics theory in the future. For example, it helps anticipate research on integrating various MLs to understand which time-series features are important for prediction and identifies the importance of certain cross-sectional factors.

Additionally, researchers have long attempted to analyze textual data contained in various financial disclosures. A well-known example of this is sentiment analysis. Ingram and Frazier (1983) analyzed the relationship between the narrative data of accounting reports and corporate performance. Since then, researchers have highlighted the importance of sentiment analysis of various narrative data such as financial reports, CEOs’ letters to shareholders, and audit reports, with active related research appearing in top accounting and financial journals (Kothari, Li and Short, 2009; Feldman, Govindaraj, Livnat, and Segal, 2010; Bochkay, Hales and Chava, 2020). However, according to Bochkay, Brown, Leone and Tucker (2022), 97.4% of the literature on sentiment analysis published in top-level accounting journals in the last decade use the dictionary method, and few studies have used deep learning-based sentiment analysis. ML methods consider context, unlike the dictionary method, and the accuracy of sentiment analysis increases from 73.49% to 82.62% on average when switching from the dictionary method to traditional machine learning and from 82.62% to 87.18% when switching from traditional machine learning to deep learning (Hartmann, Heitmann, Siebert and Schamp, 2022). Therefore, more accurate analysis can be expected when NLP technology is applied to textual data analysis in the accounting and financial fields.

Another approach is behavioral finance, or applying psychology to financial phenomena. Market behavior has many commonalities with the individual decision-making process, and scholars perceive that the market does not always show rational behavior, just as all humans are not rational (De Bondt and Thaler, 1985). Behavioral finance also has a long research history, and many studies continue to attempt to interpret financial market anomalies in terms of behavioral finance (Barberis and Thaler, 2003; Ham, Ryu and Webb, 2022). While many financial market factors have already been revealed in previous examinations, current knowledge may only be the tip of the iceberg, and there will be countless factors required to explain the market. Therefore, future research should focus on providing knowledge to better understand companies and financial markets. <br>

<br>
### References

Addoum, J., Korniotis, G., & Kumar, A. (2017). Stature, obesity, and portfolio choice. _Management Science_, 63(10), 3393-3413.

Ban, G., El Karoui, N., & Lim, A. (2018), Machine learning and portfolio optimization. _Management Science_, 64(3), 1136-1154.

Barberis, N. & Thaler, R. (2003). A survey of behavioral finance, _Handbook of the Economics of Finance_, Vol. 1, pp. 1053-1128.

Bassi, A., Colacito, R. & Fulghieri, P. (2013). O sole mio: An experimental analysis of weather and risk attitudes in financial decisions. _Review of Financial Studies_, 26(7), 1824-1852.

Best, M. & Grauer, R. (1991) On the sensitivity of mean-variance-efficient portfolios to changes in asset means: Some analytical and computational results. _Review of Financial Studies_, 4(2), 315-342.

Black, F. & Litterman, R. (1990) Asset Allocation: Combining investor views with market equilibrium. _Goldman Sachs Fixed Income Research_, 115.

Bochkay, K., Hales, J., & Chava, S. (2020). Hyperbole or reality? Investor response to extreme language in earnings conference calls. _The Accounting Review_, 95(2), 31-60.

Bochkay, K., Brown, S., Leone, A., & Tucker, J. (2022). Textual Analysis in Accounting: What’s Next? Working Paper.
Britten‐Jones, M. (1999). The sampling error in estimates of mean‐variance efficient portfolio weights. _Journal of Finance_, 54(2), 655-671.

Calmon, A., Ciocan, F., & Romero, G. (2021). Revenue management with repeated customer interactions. _Management Science_, 67(5), 2944-2963.

Capponi, A., Olafsson, S., and Zariphopoulou, T. (2022). Personalized robo-advising: Enhancing investment through client interaction. _Management Science_,  68(4), 2485-512.

Chopra, V. & Ziemba, W. (2013). The effect of errors in means, variances, and covariances on optimal portfolio choice, _Handbook of the Fundamentals of Financial Decision Making: Part I_, pp. 365-373.

Cohn, R., Lewellen, W., Lease, R., & Schlarbaum, G. (1975). Individual investor risk aversion and investment portfolio composition. _Journal of Finance_, 30(2), 605-620.

De Bondt, W. & Thaler, R. (1985). Does the stock market overreact? _Journal of Finance_, 40(3), 793-805.

Døskeland, T. & Kvaerner, J. (2022). Cancer and portfolio choice: Evidence from Norwegian Register Data. _Review of Finance_, 26(2), 407-442.

Faig, M. & Shum, P. (2002). Portfolio choice in the presence of personal illiquid projects. _Journal of Finance_, 57(1), 303-328.

Feldman, R., Govindaraj, S., Livnat, J., & Segal, B. (2010). Management’s tone change, post earnings announcement drift and accruals. _Review of Accounting Studies_, 15(4), 915-953.

Filbeck, G., Hatfield, P., & Horvath, P. (2005). Risk aversion and personality type. _Journal of Behavioral Finance_, 6(4), 170-180.

Foerster, S., Linnainmaa, J., Melze, B., & Previtero, A. (2017). Retail financial advice: Does one size fit all? _Journal of Finance_, 72(4), 1441-1482.

Grable, J. (2008). Risk tolerance, _Handbook of Consumer Finance Research, New York: Springer_, pp. 3-19.

Gu, S., Kelly, B., & Xiu, D. (2020). Empirical asset pricing via machine learning. _Review of Financial Studies_, 33(5), 2223-2273.

Ham, H., Ryu, D., & Webb, R. (2022). The effects of overnight events on daytime trading sessions. _International Review of Financial Analysis_, 102228.

Hartmann, J., Heitmann, M., Siebert, C., & Schamp, C. (2022). More than a feeling: Accuracy and application of sentiment analysis. _International Journal of Research in Marketing_. https://doi.org/10.1016/j.ijresmar.2022.05.005

Hathaway, B., Emadi, S., & Deshpande, V. (2022). Personalized priority policies in call centers using past customer interaction information. _Management Science_, 68(4), 2806-2823.

Ingram, R. & Frazier, K. (1983). Narrative disclosures in annual reports, _Journal of Business Research_, 11(1), 49-60.

Jagannathan, R. & Ma, T. (2003). Risk reduction in large portfolios: Why imposing the wrong constraints helps. _Journal of Finance_, 58(4), 1651-1683.

Kimball, M., Shapiro, M, Shumway, T., & Zhang, J. (2020). Portfolio rebalancing in general equilibrium. _Journal of Financial Economics_, 135(3), 816-834. 

Kothari, S., Li, X., & Short, J. (2009). The effect of disclosures by management, analysts, and business press on cost of capital, return volatility, and analyst forecasts: A study using content analysis. _The Accounting Review_, 84(5), 1639-1670.

Kumar, A., Page, J., & Spalt, O. (2011). Religious beliefs, gambling attitudes, and financial market outcomes. _Journal of Financial Economics_, 102(3), 671-708.

Latané, H.  (1960). Individual risk preference in portfolio selection. _Journal of Finance_, 15(1), 45-52.

Ledoit, O., & Wolf, M. (2003). Improved estimation of the covariance matrix of stock returns with an application to portfolio selection. _Journal of Empirical Finance_, 10(5), 603-621.

Lopez, C.J., Babcic, S., & De La Ossa, A. (2015). Advice goes virtual: how new digital investment services are changing the wealth management landscape. _Journal of Financial Perspectives_, 3(3).

Madhavan, A. (2000). Market microstructure: A survey. _Journal of Financial Markets_, 3(3), 205-258.

Markowitz, H. (1952). Portfolio selection. _Journal of Finance_, 7(1), 77-91.

Masters, S. (2003). Rebalancing. _Journal of Portfolio Management_, 29(3), 52-57.

Michaud, R. (1989). The Markowitz Optimization Enigma: Is ‘optimized’ optimal? _Financial Analysts Journal_, 45(1), 31-42.

O’hara, M. (2015). High frequency market microstructure. _Journal of Financial Economics_, 116(2), 257-270.

Rosen, H. & Wu, S. (2004). Portfolio choice and health status. _Journal of Financial Economics_, 72(3), 457-484.

Sironi, P. (2016). _FinTech innovation: from robo-advisors to goal based investing and gamification._ John Wiley & Sons.

Sun, W., Fan, A., Chen, L., Schouwenaars, T., & Albota, M. (2006). Optimal rebalancing for institutional portfolios. _Journal of Portfolio Management_, 3(2), 33-43.

Tsoukalas, G., Wang, J., & Giesecke, K. (2019). Dynamic portfolio execution. _Management Science_, 65(5), 2015-2040.
