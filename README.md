<details>
<summary>A. Momentum Trading</summary>
<!--Momentum Trading-->

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

[中文](chn/Time-Series_and_Cross-Sectional_Momentum.md) [英文](eng/[01]%20ssrn-4675565.pdf)
</details>

<details>
<summary>2. Trading with the Momentum Transformer: An Intelligent and Interpretable Architecture</summary>

本研究提出了一種基於注意力機制的深度學習架構——**Momentum Transformer**，用於時間序列動量交易策略。我們的方法結合了 Transformer 的全局時間依賴性學習能力與 LSTM（Long Short-Term Memory）的局部模式識別能力，以提升交易決策的準確性和穩健性。 

相較於傳統的 LSTM 架構與基準動量策略，Momentum Transformer 顯示出顯著的性能提升，尤其在市場環境變化（regime change）期間仍能保持卓越表現。該模型透過多頭注意力機制（Multi-Head Attention）學習市場在不同時間尺度上的模式變化，並利用可解釋性網絡（Variable Selection Network, VSN）識別最重要的市場特徵。回測結果表明，Momentum Transformer 在 1995–2020 年期間的風險調整後收益（夏普比率）相較於 LSTM 提升 50%，而在 2015–2020 年市場非平穩時期的提升幅度更達 109%。此外，在 SARS-CoV-2（COVID-19）市場崩盤期間，Momentum Transformer 能夠迅速適應市場轉折，捕捉新趨勢，展現出優異的市場適應能力。

透過引入變化點檢測（Change Point Detection, CPD）模組，我們進一步提升了 Momentum Transformer 的表現，使其在市場 regime 轉變時更加靈活。同時，我們發現 Momentum Transformer 對交易成本較不敏感，即便在較高的交易成本環境下仍能保持穩定的回報表現。

總結而言，Momentum Transformer 透過結合深度學習技術與可解釋性機制，提供了一種更智能、更穩健的動量交易策略，並在市場極端環境下保持競爭力。我們的研究為量化金融中的深度學習應用提供了新的視角，未來可進一步擴展至股票市場、跨資產交易及其他因子驅動的投資策略。
</details>

<!--Momentum Trading-->
</details>

---

<details>
<summary>B. Mean Reversion Trading</summary>
<!--Mean Reversion Trading-->

<!--Mean Reversion Trading-->
</details>

---

<details>
<summary>C. Grid Trading</summary>
<!--Grid Trading-->

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

<!--Quantitative Trading-->
</details>

---

<details>
<summary>F. Machine Learning Strategies</summary>
<!--Machine Learning Strategies-->

<!--Machine Learning Strategies-->
</details>

<details>
<summary>G. High-Frequency Trading</summary>
<!--High-Frequency Trading-->

<!--High-Frequency Trading-->
</details>

---

<details>
<summary>H. Spread Trading</summary>
<!--Spread Trading-->

<!--Spread Trading-->
</details>

---

<details>
<summary>I. Cross-Currency Strategies</summary>
<!--Cross-Currency Strategies-->

<!--Cross-Currency Strategies-->
</details>

---

<details>
<summary>J. Cross-Exchange Strategies</summary>
<!--Cross-Exchange Strategies-->

<!--Cross-Exchange Strategies-->
</details>

---

<details>
<summary>K. Market Analysis</summary>

<details>
<summary>1. Factors Influencing Cryptocurrency Prices: Evidence from Bitcoin, Ethereum, Dash, Litcoin, and Monero</summary>

本研究探討影響加密貨幣價格的因素，涵蓋比特幣（Bitcoin）、以太坊（Ethereum）、達世幣（Dash）、萊特幣（Litecoin）和門羅幣（Monero），使用 2010-2018 年的每週數據，並透過 **自回歸分佈式滯後模型（ARDL）** 分析短期與長期影響因素。研究結果顯示，加密貨幣價格主要受到 **市場回報率（Market Beta）、交易量（Trading Volume）、市場波動性（Volatility）與吸引力（Attractiveness，如 Google 搜尋趨勢）** 影響。此外，標準普爾 500 指數（S&P 500）對比特幣和以太坊價格在長期內具有微弱影響。短期內市場波動性對價格影響更大，而長期內吸引力成為主要決定因素。本研究為投資者與政策制定者提供了對加密貨幣市場價格決定因素的新見解。

[中文](chn/Factors_Influencing_Cryptocurrency_Prices.md) [英文](eng/[12a]%20vol2-no2-1.pdf)
</details>

<!--Market Analysis-->
</details>