A. [Momentum Trading](#A)<br>
B. [Mean Reversion Trading](#B)<br>
C. [Arbitrage Trading](#C)<br>
D. [Quantitative Trading](#D)<br>
E. [Machine Learning Trading](#E)<br>
F. [High-Frequency Trading](#F)<br>
G. [Market Study](#G)<br>

---

<!-- #region Momentum Trading -->

<a name="A"></a>
A. Momentum Trading

<!-- #region A1 -->

<details>
<summary>1. (2024) Time-Series and Cross- Sectional Momentum in the Cryptocurrency Market: A Comprehensive Analysis under Realistic Assumptions</summary><br>

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

<!-- #endregion -->

---

<!-- #region Mean Reversion Trading -->

<a name="B"></a>
B. Mean Reversion Trading

<!-- #region B1 -->

<details>
<summary>1. (2022) The Feasibility of Grid Trading Approach for Bitcoin Based on Backtesting</summary><br>

當前，以比特幣為代表的加密貨幣吸引了投資者的廣泛關注。比特幣的本質與法定貨幣或傳統金融資產不同，其高波動性導致比特幣交易市場存在較大的潛在金融風險。因此，研究比特幣市場的波動性具有重要的現實意義。本研究探討了網格交易策略在高波動性市場（如比特幣市場）中的可行性與有效性。  

基於對比特幣從**2019年7月至2021年7月**的日交易數據進行分析，研究結果表明，網格交易策略在比特幣交易市場是可行的。在此基礎上，本研究進一步探討了**初始倉位價格、網格價格上限、網格價格下限、上層網格數量、下層網格數量**等因素對比特幣網格交易收益率的影響，並基於回測方法進行驗證。研究結果顯示，當初始倉位價格設為**35,000**，網格價格上限為**50,000**，網格價格下限為**6,000**，上層網格數量為**20**，下層網格數量為**1或2**時，網格交易能獲得最高的收益率。  

[[中文]](chn/[09]Grid_Trading_Approach.md) [[英文]](eng/[09]eai.18-11-2022.2327164.pdf)
</details>


<!-- #region B2 -->

<details>
<summary>2. (2024) Cryptocurrency Market-making: Improving Grid Trading Strategies in Bitcoin</summary><br>

在不斷變化的加密貨幣市場中，**網格交易策略（Grid Trading）** 已成為促進流動性和穩定性的關鍵工具。本研究分析了 **ByBit 交易所** 上現有的網格交易策略，並探討了 **機器學習模型**（如 **隨機森林**（Random Forest）和 **長短期記憶網絡**（LSTM））對於優化這些策略參數的可行性。此外，研究還引入了一種 **新的避險策略（hedging strategy）**，旨在在降低風險的同時最大化回報。  

透過 **自訂回測系統（backtesting system）** 進行測試，結果顯示：  
1. **機器學習整合未能顯著優於傳統網格交易方法**，表明在此環境下，機器學習模型的應用仍需進一步探索與改進。  
2. **新避險策略表現優於單純持有比特幣（holding Bitcoin）**，展現出較高的回報率與風險管理能力。  

本研究為進一步優化網格交易策略、改進特徵工程（feature engineering）、以及在 **即時市場（live market）** 中進行測試提供了理論基礎與實證分析。

[[中文]](chn/[10]Improving_Grid_Trading.md) [[英文]](eng/[10]Cryptocurrency%20Market-making_%20Improving%20Grid%20Trading%20Strategies%20in%20Bitcoin.pdf)
</details>

<!-- #endregion -->

<!-- #endregion -->


<!-- #endregion -->

---

<!-- #region Arbitrage Trading -->

<a name="C"></a>
C. Arbitrage Trading

<!-- #region C1 -->
<details>
<summary>1. (2024) Optimal Market-Neutral Multivariate Pair Trading on the Cryptocurrency Platform</summary><br>

本研究提出了一種創新的套利方法，用於多變量配對交易（Multivariate Pair Trading），並將其稱為最佳交易技術（Optimal Trading Technique, OTT）。該方法利用一組與加密貨幣掛鉤的法定貨幣（fiat currency bucket）來監測和同時挖掘交易機會。為了解決來自多個交易信號的數量衝突，研究設計了一種**雙目標凸優化（bi-objective convex optimization）**方法，以平衡投資者對盈利和風險的偏好。本方法包含可調整的參數，如波動懲罰（volatility penalties）和交易閾值（action thresholds），以適應不同風險承受能力的投資者。

在 2020 至 2022 年的歷史數據回測中（涵蓋牛市和熊市），OTT 方法實現了年化盈利率 15.49%，並在後疫情時期對主要加密貨幣進行的額外測試中，驗證了該模型的穩健性與有效性。與傳統的「距離方法（Distance Method, DM）」相比，OTT 方法更具優勢，因為它能夠避免持有高波動性的中間加密貨幣，並且不需要借貸來進行做空交易（shorting）。此外，該套利策略提供了一種新的交易視角，不依賴於外部市場的變化，而是通過資產之間的價差變動來獲取利潤。

然而，本研究亦強調加密貨幣投資的高風險性，市場波動劇烈且可能帶來潛在損失。因此，投資者在應用該策略時應謹慎評估風險，並充分理解市場條件對交易結果的影響。

[[中文]](chn/[06]Optimal_Market-Neutral_Multivariate_Pair.md) [[英文]](eng/[06]2405.15461v5.pdf)
</details>
<!-- #endregion -->

<!-- #region C2 -->

<details>
<summary>2. (2023) Copula-Based Trading of Cointegrated Cryptocurrency Pairs</summary><br>

**配對交易（Pairs Trading）**是一種廣為人知的**演算法交易策略**，利用兩個或多個資產之間的**歷史價格關係**，當此關係出現異常變化時，即觸發交易信號，並在價格關係回歸正常時平倉以獲取套利收益。在**去中心化的加密貨幣市場**中，配對交易策略可以帶來潛在的套利機會，主要包括**交易所間套利（Exchange-to-Exchange Arbitrage）**和**統計套利（Statistical Arbitrage）**。然而，基於交易所間套利的統計套利策略**風險較高且實施困難**，相比之下，純統計套利策略風險較低，仍然具有顯著的獲利潛力。  

[[中文]](chn/[07]Copula-Based_Trading.md) [[英文]](eng/[07]WP_wps-202301-0004.pdf)
</details>

<!-- #endregion -->

<!-- #region C3 -->

<details>
<summary>3. (2024) Optimized pairs-trading strategies in the cryptocurrencies market using genetic algorithms and cointegration</summary><br>

加密資產市場以其高度波動性和風險性而聞名。在此背景下，市場中立型策略（如配對交易策略，Pairs Trading）可能具有一定的應用價值。本文專注於應用配對交易策略，並選取**209種加密資產**（樣本期從**2021年8月1日至2024年1月31日**）進行實證研究。我們結合了**計量經濟學與機器學習技術**，以區別於現有文獻。通過**共整合檢驗**與**誤差修正模型 (ECM)**，我們篩選出**229對適用於配對交易的資產對**。

為了進一步優化策略，我們使用了**遺傳算法 (Genetic Algorithm)** 和**配對聚類 (Pair Clustering)**，測試了**四種策略**，包括標準閾值與優化閾值的比較。結果顯示，加密資產市場中存在可獲利的**共整合關係**，從而證明市場在短期內可能存在**非效率性**。即使最優策略仍然具有一定風險（**最大回撤中位數為29%**），但在回測期間，每個資產對的**年化夏普比率 (Sharpe Ratio) 平均可達1.53**。

[[中文]](chn/[08]Optimized_pairs-trading_strategies.md) [[英文]](eng/[08]WP_2024-11.pdf)
</details>

<!-- #endregion -->

<!-- #region C4 -->
<details>
<summary>4. (2019) Lead-Lag Relationship between Bitcoin and Ethereum: Evidence from Hourly and Daily Data</summary><br>

### 摘要 (*Summary*)

本研究探討了比特幣 (BTC) 與以太坊 (ETH) 之間的**領先-滯後（Lead-Lag）關係**，以識別這兩種主要加密貨幣的價格領導模式。傳統的市場信息流動研究主要集中在**現貨與期貨市場**的相互影響，而加密貨幣市場的價格傳導機制仍然缺乏深入研究。因此，本研究利用**VECM、Granger 因果檢驗、ARMA、ARDL 及小波相干性分析（Wavelet Coherence）**等多種統計方法，對 2017 年 8 月至 2018 年 9 月期間的**小時與每日數據**進行分析。

主要研究結果顯示：
1. **比特幣與以太坊之間存在雙向因果關係**，表明兩者在價格變動上互相影響，沒有明顯的單一價格領導者。
2. **價格發現過程的有效性較高**，使得日內交易者難以利用 BTC 和 ETH 之間的價格變動來獲取套利機會。
3. **加密貨幣市場內部的價格聯動性明顯**，進一步證實這些資產之間的市場互動關係。

本研究為加密貨幣市場的信息流動與價格形成機制提供了實證證據，對於市場參與者、投資者及監管機構而言，理解這種雙向影響關係有助於優化投資決策並提升市場監管效能。

[[中文]](chn/[37]Lead-Lag_BTC_ETH.md) [[英文]](eng/[37]RIBAFLLRG1.pdf)
</details>
<!-- #endregion -->


<!-- #endregion -->

---

<!-- #region Quantitative Trading -->

<a name="D"></a>
D. Quantitative Trading


<!-- #endregion -->

---

<!-- #region Machine Learning Trading -->

<a name="E"></a>
E. Machine Learning Trading

<!-- #region E1 -->

<details>
<summary>1. (2022) Trading with the Momentum Transformer: An Intelligent and Interpretable Architecture</summary><br>

本研究提出了一種基於注意力機制的深度學習架構——**Momentum Transformer**，用於時間序列動量交易策略。我們的方法結合了 Transformer 的全局時間依賴性學習能力與 LSTM（Long Short-Term Memory）的局部模式識別能力，以提升交易決策的準確性和穩健性。 

相較於傳統的 LSTM 架構與基準動量策略，Momentum Transformer 顯示出顯著的性能提升，尤其在市場環境變化（regime change）期間仍能保持卓越表現。該模型透過多頭注意力機制（Multi-Head Attention）學習市場在不同時間尺度上的模式變化，並利用可解釋性網絡（Variable Selection Network, VSN）識別最重要的市場特徵。回測結果表明，Momentum Transformer 在 1995–2020 年期間的風險調整後收益（夏普比率）相較於 LSTM 提升 50%，而在 2015–2020 年市場非平穩時期的提升幅度更達 109%。此外，在 SARS-CoV-2（COVID-19）市場崩盤期間，Momentum Transformer 能夠迅速適應市場轉折，捕捉新趨勢，展現出優異的市場適應能力。

透過引入變化點檢測（Change Point Detection, CPD）模組，我們進一步提升了 Momentum Transformer 的表現，使其在市場 regime 轉變時更加靈活。同時，我們發現 Momentum Transformer 對交易成本較不敏感，即便在較高的交易成本環境下仍能保持穩定的回報表現。

總結而言，Momentum Transformer 透過結合深度學習技術與可解釋性機制，提供了一種更智能、更穩健的動量交易策略，並在市場極端環境下保持競爭力。我們的研究為量化金融中的深度學習應用提供了新的視角，未來可進一步擴展至股票市場、跨資產交易及其他因子驅動的投資策略。

[[中文]](chn/[02]Momentum_Transformer.md) [[英文]](eng/[02]2112.08534v3.pdf)
</details>

<!-- #endregion -->

<!-- #region E2 -->

<details>
<summary>2. (2023) Transfer Ranking in Finance: Applications to Cross-Sectional Momentum with Data Scarcity</summary><br>

現代跨橫斷面交易策略中，結合了**深度學習 (Deep Learning, DL)** 的先進神經網絡模型在歷史數據充足的成熟資產上能夠超越傳統方法。然而，當應用於交易數據有限的標的時，這些模型容易**過擬合 (overfitting)**，導致績效下降。

本研究提出了一種新方法——**Fused Encoder Networks (FEN)**，這是一種混合的參數共享**遷移學習排名模型 (Transfer Ranking Model)**。該模型利用 **編碼器-注意力模塊 (encoder-attention module)** 來融合從大數據集（源數據）中提取的信息，以及針對目標數據集的專用模塊，以提升模型的**泛化能力 (generalizability)**。

**方法與創新**：  
- 採用 **自注意力機制 (self-attention mechanism)**，允許模型在訓練和推理過程中考慮不同資產間的相互作用。
- 透過混合學習策略，在源數據集（例如外匯數據）上訓練部分模型，並與針對目標數據（例如加密貨幣）訓練的模組相結合，從而降低過擬合風險。

**實驗與結果**：  
- 研究將 FEN 應用於 **前十大加密貨幣的動能交易策略**（基於市值排名），並與現有最先進的基準方法進行比較。  
- 在大多數評估指標上，FEN **優於其他方法**，特別是在風險調整後回報方面，如 **Sharpe Ratio** 顯著提高。  
- 即使考慮**高交易成本**（如加密貨幣市場的手續費與滑點），FEN 仍能保持優異的交易表現。  

**結論與影響**：  
FEN 有效解決了**數據稀缺環境下的金融交易建模問題**，提供了一種適用於跨市場應用的**遷移學習框架**，並為使用 **Transformer 自注意力機制** 提升金融市場的學習排序模型提供了新方向。

[[中文]](chn/[03]Transfer_Ranking_in_Finance.md) [[英文]](eng/[03]2208.09968v3.pdf)
</details>

<!-- #endregion -->

<!-- #region E3 -->

<details>
<summary>3. (2024) Reinforcement Learning Pair Trading: A Dynamic Scaling Approach</summary><br>

加密貨幣是一種基於密碼學的數字資產，其價格極端波動，全球每日交易量約達 **700 億美元**。由於市場的高波動性，使得加密貨幣交易變得極具挑戰性。本研究探討**強化學習（Reinforcement Learning, RL）**是否能夠提升加密貨幣演算法交易的決策能力，並與傳統交易方法進行比較。  

為解決此問題，我們將**強化學習與統計套利交易技術——配對交易（Pair Trading）**相結合，該技術利用統計相關資產間的價格差異進行交易。我們構建了**RL 交易環境**，並訓練 RL 代理（agent）來決定何時及如何交易加密貨幣對。我們針對強化學習開發了**新的獎勵設計（reward shaping）**及**觀察/動作空間（observation/action spaces）**，以提升交易決策的智能化程度。  

在實驗中，我們利用**BTC-GBP 和 BTC-EUR** 交易對的價格數據（時間間隔為 **1 分鐘，n = 263,520**）進行測試。結果顯示，**傳統的非 RL 配對交易技術年化利潤為 8.33%**，而**基於 RL 的配對交易技術年化利潤範圍為 9.94% 至 31.53%**，具體收益率取決於所選用的 RL 演算法。  

實驗結果表明，在**高波動市場**（如加密貨幣市場）中，RL 方法在交易決策上能顯著優於人工或傳統配對交易技術，並能夠適應市場變化，提高交易績效。

[[中文]](chn/[05]Reinforcement_Learning_Pair_Trading.md) [[英文]](eng/[05]jrfm-17-00555.pdf)
</details>

<!-- #endregion -->

<!-- #endregion -->

---

<!-- #region High-Frequency Trading -->

<a name="F"></a>
F. High-Frequency Trading


<!-- #endregion -->

---

<!-- #region Market Study -->

<a name="G"></a>
G. Market Study

<!-- #region G1 -->

<details>
<summary>1. (2018) Factors Influencing Cryptocurrency Prices: Evidence from Bitcoin, Ethereum, Dash, Litcoin, and Monero</summary><br>

本研究探討影響加密貨幣價格的因素，涵蓋比特幣（Bitcoin）、以太坊（Ethereum）、達世幣（Dash）、萊特幣（Litecoin）和門羅幣（Monero），使用 2010-2018 年的每週數據，並透過 **自回歸分佈式滯後模型（ARDL）** 分析短期與長期影響因素。研究結果顯示，加密貨幣價格主要受到 **市場回報率（Market Beta）、交易量（Trading Volume）、市場波動性（Volatility）與吸引力（Attractiveness，如 Google 搜尋趨勢）** 影響。此外，標準普爾 500 指數（S&P 500）對比特幣和以太坊價格在長期內具有微弱影響。短期內市場波動性對價格影響更大，而長期內吸引力成為主要決定因素。本研究為投資者與政策制定者提供了對加密貨幣市場價格決定因素的新見解。

[[中文]](chn/[35]Factors_Influencing_Cryptocurrency_Prices.md) [[英文]](eng/[35]vol2-no2-1.pdf)
</details>

<!-- #endregion -->

<!-- #region G2 -->
<details>
<summary>2. (2022) Cryptocurrencies: from characteristics to behaviours</summary><br>

隨著加密貨幣市場的快速發展，其高波動性與缺乏監管的特性使其成為高風險投資工具。本研究探討加密貨幣投資者的特徵、動機與市場行為，並分析金融機構與監管機構對加密貨幣的態度。透過問卷調查與訪談，研究發現投資者可分為兩類：一類主要投資於比特幣等主流貨幣，通常擁有較高收入、較長投資經驗，並對市場有較高信心；另一類則投資於低價替代幣（Altcoins），收入較低，投資時間較短，且獲利與滿意度相對較低。投資者主要關注低交易成本與全球支付的便利性，但也擔憂市場詐騙與監管缺失。大多數投資者認為未來監管將提升市場穩定性與信任度，但對價格影響的看法不一。此外，金融機構普遍對加密貨幣持保守態度，擔憂與非法活動的關聯，但對區塊鏈技術表現出一定興趣。本研究結論顯示，加密貨幣市場雖存在諸多風險，但投資者對其前景仍抱持高度興趣，監管政策的發展將成為影響市場走向的關鍵因素。

[[中文]](chn/[36]Cryptocurrencies_from_characteristics_to_behaviour.md) [[英文]](eng/[36]Cryptocurrencies_from_characteristics_to_behaviour.pdf)
</details>
<!-- #endregion -->

<!-- #region G3 -->
<details>
<summary>3. (2018) Information Transmission Between Cryptocurrencies: Does Bitcoin Rule the Cryptocurrency World?</summary><br>

**比特幣（Bitcoin）、萊特幣（Litecoin）、瑞波幣（Ripple）、以太坊（Ethereum）和比特幣現金（Bitcoin Cash）**之間的信息傳播，分析它們之間的方向性、強度和持續性。研究採用**向量自回歸（VAR）模型**，並計算**Geweke 反饋測度**與**廣義脈衝響應函數**。  

結果顯示，大部分信息傳播是**當日發生的（即同一天內）**，而滯後影響較少。與傳統認知不同，**比特幣並未主導信息流**，反而是其他加密貨幣（尤其是萊特幣）對比特幣的價格變動有較大的滯後影響。此外，在較新的樣本（2017-2018年）中，比特幣對市場衝擊有**過度反應**，並在次日進行修正。  

這些發現顯示，比特幣雖然在市值和交易量上具領先地位，但在信息傳播方面並不佔據主導地位。本研究對於理解加密貨幣市場的信息流動特性，以及不同貨幣之間的相互影響，具有重要意義。

[[中文]](chn/[38]Info_Transmission_Crypto.md) [[英文]](eng/[38]27_07_2018_332-1024-4-PB.pdf)
</details>
<!-- #endregion -->

<!-- #region G4 -->
<details>
<summary>4. (2017) Where is the information on USD/Bitcoin hourly price movements?</summary><br>

本研究分析 **美元/比特幣（USD/BTC）市場的價格發現過程**，涵蓋 **Mt.Gox 破產後（2014年3月1日）至 Bitfinex 遭駭事件後（2016年11月30日）** 的市場變化。研究運用 **Geweke 反饋測度（Geweke feedback measures）**，以**每小時回報率**進行雙變量估計，探討市場資訊傳遞機制。

**主要發現**：
1. **市場資訊傳遞效率**：四大主要交易所（Bitfinex、Bitstamp、BTC-e、ItBit）間資訊可在 **一小時內傳遞完畢**，但較小的交易所存在滯後反應。
2. **市場資訊流向**：
   - **Bitfinex 是主要的價格資訊發送者**，其滯後反饋占市場資訊流的 **18.29%**，市場對 Bitfinex 的資訊回饋僅 **0.60%**。
   - 其他較小的交易所（minor exchanges）對市場資訊的影響微乎其微，反應也較為延遲。
3. **交易量與市場整合度**：
   - **交易量越大，市場資訊傳遞越快**。
   - **主要交易所的波動性有助於價格資訊傳遞**，而較小交易所的波動性可能引入市場雜訊。
4. **資訊傳遞模式**：
   - 即時反饋（contemporaneous feedback）是資訊傳遞的主要機制，約占 **75% 以上**。
   - 小型交易所主要透過滯後反饋（lagged feedback）獲取資訊，顯示它們是「**衛星交易所（satellite exchanges）**」。

本研究顯示，比特幣市場的價格發現過程主要由交易量最大且波動性較高的交易所主導，提供了對**比特幣市場微觀結構**的深入理解，並對**監管機構、交易策略開發者和市場參與者**具有參考價值。

[[中文]](chn/[39]information_price_movements.md) [[英文]](eng/[39]CeBERwp2017_05.pdf)
</details>
<!-- #endregion -->

<!-- #endregion -->
---

<!-- #region X0 -->
<details>
<summary></summary><br>

[[中文]](chn) [[英文]](eng)
</details>
<!-- #endregion -->
