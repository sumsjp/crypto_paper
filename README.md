<details>
<summary>A. Momentum Trading</summary>
<!--Momentum Trading-->
<br>

<!-- #region A1 -->

<details>
<summary>1. Time-Series and Cross- Sectional Momentum in the Cryptocurrency Market: A Comprehensive Analysis under Realistic Assumptions</summary>

本研究針對加密貨幣市場的 **時間序列動能（Time-Series Momentum）** 和 **橫截面動能（Cross-Sectional Momentum）** 進行了全面分析，並考慮了過去研究所忽略的現實市場因素，如 **交易成本** 和 **日內價格波動**，以更準確評估動能策略的有效性。

主要發現包括：

1. **時間序列動能效應顯著**：市場回報的時間序列動能效果較強，並在上升市場表現最佳。然而，空頭部位的表現不佳，意味著該效應主要來自多頭市場。
2. **橫截面動能證據較弱**：不同加密貨幣之間的橫截面動能效果不明顯，且部分策略因高跳動風險（Jump Risk）導致重大損失或清算。
3. **傳統統計方法可能誤導結論**：在高波動市場，如加密貨幣市場，僅透過 t 檢定檢視平均報酬無法準確衡量長期獲利能力，應使用 **對數回報（Log Return）** 進行檢測。
4. **贏家效應明顯，輸家常出現反轉**：動能效應主要集中在「贏家」資產上，而「輸家」資產往往會出現反彈，導致空頭策略承受高額風險。
5. **過度反應（Overreaction）可能是主要動力**：市場中的投資者對於新聞或社交媒體訊息的過度反應，可能是驅動動能效應的主要原因，但具體影響因素尚不清楚。

整體而言，本研究指出，時間序列動能策略在加密貨幣市場具備一定的可行性，但 **高風險與市場條件變化使得動能策略的長期穩健性存疑**。此外，由於市場仍處於發展階段，這些結論可能在未來市場成熟時有所改變。

[[中文]](chn/[01]Time-Series_and_Cross-Sectional_Momentum.md) [[英文]](eng/[01]ssrn-4675565.pdf)
</details>

<!-- #endregion -->

<!--Momentum Trading-->
</details>

---

<details>
<summary>B. Mean Reversion Trading</summary>
<!--Mean Reversion Trading-->
<br>

<!-- #region X0 -->

<details>
<summary></summary>

[[中文]](chn) [[英文]](eng)
</details>

<!-- #endregion -->

<!--Mean Reversion Trading-->
</details>

---

<details>
<summary>C. Grid Trading</summary>
<!--Grid Trading-->
<br>

<!--Grid Trading-->
</details>

---

<details>
<summary>D. Arbitrage Trading</summary>
<!--Arbitrage Trading-->

<!--Arbitrage Trading-->
</details>

---

<details>
<summary>E. Quantitative Trading</summary>
<!--Quantitative Trading-->
<br>

<!--Quantitative Trading-->
</details>

---

F. Machine Learning Strategies
<!--Machine Learning Strategies-->

<!-- #region F1 -->

<details>
<summary>1. Trading with the Momentum Transformer: An Intelligent and Interpretable Architecture</summary>

本研究提出了一種基於注意力機制的深度學習架構——**Momentum Transformer**，用於時間序列動量交易策略。我們的方法結合了 Transformer 的全局時間依賴性學習能力與 LSTM（Long Short-Term Memory）的局部模式識別能力，以提升交易決策的準確性和穩健性。 

相較於傳統的 LSTM 架構與基準動量策略，Momentum Transformer 顯示出顯著的性能提升，尤其在市場環境變化（regime change）期間仍能保持卓越表現。該模型透過多頭注意力機制（Multi-Head Attention）學習市場在不同時間尺度上的模式變化，並利用可解釋性網絡（Variable Selection Network, VSN）識別最重要的市場特徵。回測結果表明，Momentum Transformer 在 1995–2020 年期間的風險調整後收益（夏普比率）相較於 LSTM 提升 50%，而在 2015–2020 年市場非平穩時期的提升幅度更達 109%。此外，在 SARS-CoV-2（COVID-19）市場崩盤期間，Momentum Transformer 能夠迅速適應市場轉折，捕捉新趨勢，展現出優異的市場適應能力。

透過引入變化點檢測（Change Point Detection, CPD）模組，我們進一步提升了 Momentum Transformer 的表現，使其在市場 regime 轉變時更加靈活。同時，我們發現 Momentum Transformer 對交易成本較不敏感，即便在較高的交易成本環境下仍能保持穩定的回報表現。

總結而言，Momentum Transformer 透過結合深度學習技術與可解釋性機制，提供了一種更智能、更穩健的動量交易策略，並在市場極端環境下保持競爭力。我們的研究為量化金融中的深度學習應用提供了新的視角，未來可進一步擴展至股票市場、跨資產交易及其他因子驅動的投資策略。

[[中文]](chn/[02]Momentum_Transformer.md) [[英文]](eng/[02]2112.08534v3.pdf)
</details>

<!-- #endregion -->

<!-- #region F2 -->

<!-- #region F3 -->

<details>
<summary>2. Transfer Ranking in Finance: Applications to Cross-Sectional Momentum with Data Scarcity</summary>

加密貨幣是一種基於密碼學的數字資產，其價格極端波動，全球每日交易量約達 **700 億美元**。由於市場的高波動性，使得加密貨幣交易變得極具挑戰性。本研究探討**強化學習（Reinforcement Learning, RL）**是否能夠提升加密貨幣演算法交易的決策能力，並與傳統交易方法進行比較。  

為解決此問題，我們將**強化學習與統計套利交易技術——配對交易（Pair Trading）**相結合，該技術利用統計相關資產間的價格差異進行交易。我們構建了**RL 交易環境**，並訓練 RL 代理（agent）來決定何時及如何交易加密貨幣對。我們針對強化學習開發了**新的獎勵設計（reward shaping）**及**觀察/動作空間（observation/action spaces）**，以提升交易決策的智能化程度。  

在實驗中，我們利用**BTC-GBP 和 BTC-EUR** 交易對的價格數據（時間間隔為 **1 分鐘，n = 263,520**）進行測試。結果顯示，**傳統的非 RL 配對交易技術年化利潤為 8.33%**，而**基於 RL 的配對交易技術年化利潤範圍為 9.94% 至 31.53%**，具體收益率取決於所選用的 RL 演算法。  

實驗結果表明，在**高波動市場**（如加密貨幣市場）中，RL 方法在交易決策上能顯著優於人工或傳統配對交易技術，並能夠適應市場變化，提高交易績效。

[[中文]](chn/[05]Reinforcement_Learning_Pair_Trading.md) [[英文]](eng/[05]jrfm-17-00555.pdf)
</details>

<!-- #endregion -->

<!-- #endregion -->

<!--Machine Learning Strategies-->


---

<details>
<summary>G. High-Frequency Trading</summary>
<!--High-Frequency Trading-->
<br>

<!--High-Frequency Trading-->
</details>

---

<details>
<summary>H. Spread Trading</summary>
<!--Spread Trading-->
<br>

<!--Spread Trading-->
</details>

---

<details>
<summary>I. Cross-Currency Strategies</summary>
<!--Cross-Currency Strategies-->
<br>

<!--Cross-Currency Strategies-->
</details>

---

<details>
<summary>J. Cross-Exchange Strategies</summary>
<!--Cross-Exchange Strategies-->
<br>

<!--Cross-Exchange Strategies-->
</details>

---

<details>
<summary>K. Cryto Currency Market</summary>
<!--Market Analysis-->
<br>

<!-- #region K1 -->

<details>
<summary>1. Factors Influencing Cryptocurrency Prices: Evidence from Bitcoin, Ethereum, Dash, Litcoin, and Monero</summary>

本研究探討影響加密貨幣價格的因素，涵蓋比特幣（Bitcoin）、以太坊（Ethereum）、達世幣（Dash）、萊特幣（Litecoin）和門羅幣（Monero），使用 2010-2018 年的每週數據，並透過 **自回歸分佈式滯後模型（ARDL）** 分析短期與長期影響因素。研究結果顯示，加密貨幣價格主要受到 **市場回報率（Market Beta）、交易量（Trading Volume）、市場波動性（Volatility）與吸引力（Attractiveness，如 Google 搜尋趨勢）** 影響。此外，標準普爾 500 指數（S&P 500）對比特幣和以太坊價格在長期內具有微弱影響。短期內市場波動性對價格影響更大，而長期內吸引力成為主要決定因素。本研究為投資者與政策制定者提供了對加密貨幣市場價格決定因素的新見解。

[[中文]](chn/[35]Factors_Influencing_Cryptocurrency_Prices.md) [[英文]](eng/[12a]vol2-no2-1.pdf)
</details>

<!-- #endregion -->

<!-- #region K2 -->

<details>
<summary>2. Cryptocurrencies: from characteristics to behaviours</summary>

隨著加密貨幣市場的快速發展，其高波動性與缺乏監管的特性使其成為高風險投資工具。本研究探討加密貨幣投資者的特徵、動機與市場行為，並分析金融機構與監管機構對加密貨幣的態度。透過問卷調查與訪談，研究發現投資者可分為兩類：一類主要投資於比特幣等主流貨幣，通常擁有較高收入、較長投資經驗，並對市場有較高信心；另一類則投資於低價替代幣（Altcoins），收入較低，投資時間較短，且獲利與滿意度相對較低。投資者主要關注低交易成本與全球支付的便利性，但也擔憂市場詐騙與監管缺失。大多數投資者認為未來監管將提升市場穩定性與信任度，但對價格影響的看法不一。此外，金融機構普遍對加密貨幣持保守態度，擔憂與非法活動的關聯，但對區塊鏈技術表現出一定興趣。本研究結論顯示，加密貨幣市場雖存在諸多風險，但投資者對其前景仍抱持高度興趣，監管政策的發展將成為影響市場走向的關鍵因素。

[[中文]](chn/[36]Cryptocurrencies_from_characteristics_to_behaviour.md) [[英文]](eng/[36]Cryptocurrencies_from_characteristics_to_behaviour.pdf)
</details>

<!-- #endregion -->

<!--Market Analysis-->
</details>