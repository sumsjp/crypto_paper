[TOC]

## Factors Influencing Cryptocurrency Prices: Evidence from Bitcoin, Ethereum, Dash, Litecoin, and Monero

### 1. **簡介**
本研究探討影響加密貨幣價格的因素，涵蓋比特幣（Bitcoin）、以太坊（Ethereum）、達世幣（Dash）、萊特幣（Litecoin）和門羅幣（Monero），使用 2010-2018 年的每週數據，並透過**自回歸分佈式滯後模型（ARDL）分析短期與長期影響因素。研究結果顯示，加密貨幣價格主要受到市場回報率（Market Beta）、交易量（Trading Volume）、市場波動性（Volatility）與吸引力（Attractiveness，如 Google 搜尋趨勢）**影響。此外，標準普爾 500 指數（S&P 500）對比特幣和以太坊價格在長期內具有微弱影響。短期內市場波動性對價格影響更大，而長期內吸引力成為主要決定因素。本研究為投資者與政策制定者提供了對加密貨幣市場價格決定因素的新見解。

本研究從**市場動態、投資者行為、傳統金融市場關聯性、短期與長期價格趨勢**等角度，分析加密貨幣價格的決定因素。研究發現：

1. **市場因素（市場回報率、交易量、波動性）** 是影響價格的關鍵因素，影響強度大於宏觀經濟變數。
2. **市場吸引力（Google Trends）** 主要影響長期價格，而非短期價格，顯示加密貨幣的認可度需要時間發酵。
3. **短期內市場波動較大，長期價格趨於均衡**，顯示投機與基本面因素的交互影響。
4. **加密貨幣與傳統金融市場有一定聯動性**，但影響較弱，顯示其仍具有一定的獨立性。
5. **監管政策可能影響市場信心**，未來研究可進一步探討法規對價格的影響。

這些角度為學術研究、投資策略制定和政策監管提供了新的視角。

### 2. **研究方法**

本研究採用 **自回歸分佈式滯後模型（Autoregressive Distributed Lag, ARDL）** 來分析影響加密貨幣價格的因素，並結合 **誤差修正模型（Error Correction Model, ECM）** 以探討短期與長期影響因素。研究方法的詳細步驟如下：

1. **數據收集**

   - 研究對象：比特幣（Bitcoin）、以太坊（Ethereum）、達世幣（Dash）、萊特幣（Litecoin）、門羅幣（Monero）。
   - 研究期間：2010-2018 年，每週數據。
   - 數據來源：
     - **加密貨幣數據**：BitInfoCharts、CoinMarketCap
     - **股票市場數據**：Yahoo Finance（標普 500 指數）
     - **宏觀經濟數據**：世界銀行（利率、匯率、黃金價格）
     - **加密貨幣吸引力**：Google Trends（搜尋趨勢）

2. **變數選擇**

   - 被解釋變數（依變數）

     ：

     - 加密貨幣價格（Bitcoin, Ethereum, Dash, Litecoin, Monero）。

   - 解釋變數（自變數）

     ：

     - 市場因素

       ：

       - **市場回報率（Market Beta, MARP）**：Crypto 50 指數（前 50 大加密貨幣的市值加權價格）。
       - **交易量（Trading Volume, MARV）**：加密貨幣市場的總交易量。
       - **市場波動性（Volatility, MARS）**：Crypto 50 指數的價格波動率。

     - 吸引力因素

       ：

       - **Google Trends 搜尋趨勢（Attractiveness, ATR）**，作為市場關注度指標。

     - 控制變數（宏觀經濟因素）

       ：

       - **標準普爾 500 指數（SP500, SPP）**：用來衡量股票市場與加密貨幣的關聯性。
       - **歐元兌美元匯率（EUR/USD, EURP）**。
       - **黃金價格（Gold Price, GOLP）**。
       - **美國利率（Interest Rate, INT）**。

3. **建立 Crypto 50 指數**

   - 依據市場市值權重，計算前 50 大加密貨幣的綜合價格、交易量與波動性，以代表整體加密貨幣市場狀況。
   - 公式：
     - Crypto 50 指數價格： CRX50=∑i=150(MCiMCCRX50×Pi)CRX50 = \sum_{i=1}^{50} \left(\frac{MC_i}{MC_{CRX50}} \times P_i\right)
     - 交易量： MARV=∑i=150VOLiMARV = \sum_{i=1}^{50} VOL_i
     - 波動性： MARS=PhPlMARS = \frac{P_h}{P_l}

4. **單根檢定（Stationarity Test）**

   - 使用 **增強型迪基-福勒（ADF）單根檢定**，確保變數為 I(0) 或 I(1)，以判定是否適合使用 ARDL 模型。

5. **ARDL 共整合檢定**

   - 透過 

     ARDL Bound Test

      來檢驗變數間是否存在長期共整合關係：

     - **短期影響**：檢視變數的即時變化對加密貨幣價格的影響。
     - **長期影響**：估算變數對價格的長期影響，計算長期乘數（Long-run multipliers）。

6. **誤差修正模型（ECM）**

   - 建立 ECM 以測試短期內價格是否回歸長期均衡：
     - 若 ECM 係數顯著且為負數，表示市場價格在短期內會回復至長期均衡。

7. **穩定性與誤差檢測**

   - **自相關檢定**（Breusch-Godfrey LM Test）。
   - **異質變異檢定**（Breusch-Pagan-Godfrey Test）。
   - **穩定性檢測**（CUSUM Test）。
   
   
   
   

