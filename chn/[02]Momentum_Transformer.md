1. [摘要](#S1)
2. [研究角度](#S2)
3. [研究方法](#S3)
4. [研究結果](#S4)
5. [研究結論](#S5)


# Trading with the Momentum Transformer: An Intelligent and Interpretable Architecture


<a name="S1"></a>
## 1. **摘要**

本研究提出了一種基於注意力機制的深度學習架構——**Momentum Transformer**，用於時間序列動量交易策略。我們的方法結合了 Transformer 的全局時間依賴性學習能力與 LSTM（Long Short-Term Memory）的局部模式識別能力，以提升交易決策的準確性和穩健性。 

相較於傳統的 LSTM 架構與基準動量策略，Momentum Transformer 顯示出顯著的性能提升，尤其在市場環境變化（regime change）期間仍能保持卓越表現。該模型透過多頭注意力機制（Multi-Head Attention）學習市場在不同時間尺度上的模式變化，並利用可解釋性網絡（Variable Selection Network, VSN）識別最重要的市場特徵。回測結果表明，Momentum Transformer 在 1995–2020 年期間的風險調整後收益（夏普比率）相較於 LSTM 提升 50%，而在 2015–2020 年市場非平穩時期的提升幅度更達 109%。此外，在 SARS-CoV-2（COVID-19）市場崩盤期間，Momentum Transformer 能夠迅速適應市場轉折，捕捉新趨勢，展現出優異的市場適應能力。

透過引入變化點檢測（Change Point Detection, CPD）模組，我們進一步提升了 Momentum Transformer 的表現，使其在市場 regime 轉變時更加靈活。同時，我們發現 Momentum Transformer 對交易成本較不敏感，即便在較高的交易成本環境下仍能保持穩定的回報表現。

總結而言，Momentum Transformer 透過結合深度學習技術與可解釋性機制，提供了一種更智能、更穩健的動量交易策略，並在市場極端環境下保持競爭力。我們的研究為量化金融中的深度學習應用提供了新的視角，未來可進一步擴展至股票市場、跨資產交易及其他因子驅動的投資策略。


<a name="S2"></a>
## 2. **研究角度**

本研究主要從以下幾個角度探討 **Momentum Transformer** 在量化交易中的應用與優勢：

**1. 深度學習在量化交易中的應用**
   - **傳統動量交易策略的局限性**：傳統時間序列動量（TSMOM）策略基於固定窗口期內的價格變動來決策，但無法靈活適應市場變化，特別是在 regime change（市場政權轉換）期間表現不佳。
   - **深度學習的引入**：先前的 **Deep Momentum Network (DMN)** 採用了 LSTM 來捕捉市場趨勢，然而 LSTM 主要適用於短期模式識別，難以有效學習長期市場趨勢。因此，本研究嘗試以 **Transformer** 取代 LSTM，以學習更長時間跨度的市場特徵。

**2. Transformer 在時間序列金融數據中的優勢**
   - **全局依賴性學習**：與 LSTM 的序列結構不同，Transformer 透過 **注意力機制（Attention Mechanism）** 直接與所有過去的時間點建立聯繫，使其更擅長捕捉長期趨勢與市場 regime 變化。
   - **多頭注意力機制（Multi-Head Attention, MHA）**：Momentum Transformer 透過 MHA 模型同時關注多個時間尺度的市場趨勢，能夠學習短期動量、長期動量及均值回歸等多種交易信號，提升策略的靈活性。

**3. 交易策略的適應性與穩健性**
   - **市場政權變化（Regime Change）適應能力**：研究關注 Momentum Transformer 在市場極端環境（如 2008 年金融危機與 2020 年 SARS-CoV-2 市場崩盤）中的表現，結果顯示該模型能夠更快適應市場變化，避免 LSTM 常見的「遺忘問題」。
   - **變化點檢測（Change Point Detection, CPD）**：研究測試了將 CPD 模組與 Momentum Transformer 結合，以增強模型的 regime 切換檢測能力，結果顯示 CPD 模組可進一步提升交易信號的穩健性，降低錯誤交易風險。

**4. 可解釋性（Interpretability）與風險管理**
   - **可解釋性強化（Variable Selection Network, VSN）**：研究關注 **Momentum Transformer** 的可解釋性，透過 VSN 觀察模型在不同市場條件下所依賴的市場指標（如短期 vs. 長期動量）。
   - **注意力機制的視覺化**：研究進一步分析了 Transformer 的注意力權重，以理解模型如何決定交易信號，以及它如何在市場變化時重新分配權重。

**5. 交易成本與實際應用**
   - **交易成本對策略績效的影響**：研究評估了 Momentum Transformer 在不同交易成本環境下的表現，並與 LSTM、傳統 Transformer 進行對比。結果顯示 Momentum Transformer 對交易成本較不敏感，能夠在 C = 3bps（基點）時仍保持良好的夏普比率。
   - **策略可行性與未來發展**：研究探討該方法是否可擴展至更廣泛的市場應用，如股票交易、跨資產組合及其他因子驅動的交易策略。

**總結**

本研究主要從 **深度學習、Transformer 時間序列建模、市場適應性、可解釋性、交易成本** 五個角度分析 Momentum Transformer 在量化交易中的應用，並驗證其在風險調整後收益、回撤控制與市場適應性方面的優勢。未來研究可進一步探索該方法在不同市場環境與多因子交易策略中的應用。


<a name="S3"></a>
## 3. **研究方法**

本研究採用**深度學習模型開發、歷史回測（Backtesting）、可解釋性分析與交易成本評估**的綜合方法來驗證 Momentum Transformer 的有效性。具體方法如下：

**1. 模型設計與開發**
本研究提出了一種新型**Momentum Transformer**，並對比多種基準模型：
- **基準模型**：
  - **傳統時間序列動量（TSMOM）策略**：基於歷史收益率進行動量投資。
  - **LSTM-based Deep Momentum Network (DMN)**：使用 LSTM 進行交易信號生成，代表過去深度學習應用於量化交易的典型方法。
  - **標準 Transformer**：使用自注意力機制（Self-Attention）進行時序建模。
  - **不同變體的 Transformer**（Decoder-Only Transformer、Convolutional Transformer、Informer）。
  - **Decoder-Only Temporal Fusion Transformer (TFT)**：一種混合 LSTM 和 Transformer 的架構，Momentum Transformer 主要基於此架構設計。

- **Momentum Transformer 設計**：
  - **多頭注意力機制（Multi-Head Attention, MHA）**：學習市場在不同時間尺度上的變化。
  - **變數選擇網絡（Variable Selection Network, VSN）**：根據市場狀態動態選擇重要因子。
  - **變化點檢測（Change Point Detection, CPD）**（可選）：用於識別市場 regime 轉換點。
  - **交易信號生成**：
    - 透過 Momentum Transformer 預測下一步的持倉權重 \( z_t \)。
    - 使用 \( tanh \) 激活函數將持倉信號限制在 \( (-1,1) \) 之間。

**2. 資料處理與特徵工程**
- **數據集**：
  - 使用 **1990–2020 年** **50 種最具流動性的連續期貨合約**（涵蓋**大宗商品、股票指數、固定收益、外匯**）。
  - 數據來源：**Pinnacle Data Corp CLC Database**。
  - 期貨合約經**比率調整（Ratio-Adjusted）**，確保價格連續性。

- **特徵工程**：
  - **標準動量因子**：不同時間尺度的回報率（每日、每月、季度、半年、年度）。
  - **技術指標**：移動平均收斂背離（MACD）指標。
  - **市場 regime 檢測**（選擇性）：變化點檢測（CPD）以量化市場 regime 轉換的嚴重程度與位置。

**3. 回測設計（Backtesting）**
- 採用**擴展窗口（Expanding Window）**方法：
  - **1990–1995 年**：訓練與驗證數據。
  - **1995–2000 年**：測試集（滾動更新）。
  - **之後每 5 年擴展訓練窗口並測試下一個 5 年區間，直到 2020 年**。

- **回測指標**：
  - **收益類指標**：
    - 年化收益率（Annualized Return）。
    - 正收益交易比例（% Positive Returns）。
  - **風險類指標**：
    - 年化波動率（Annualized Volatility）。
    - 年化下行波動率（Annualized Downside Deviation）。
    - 最大回撤（Maximum Drawdown, MDD）。
  - **風險調整收益**：
    - 夏普比率（Sharpe Ratio）。
    - 索提諾比率（Sortino Ratio）。
    - 卡爾瑪比率（Calmar Ratio）。

- **關鍵測試場景**：
  - **長期表現（1995–2020）**：衡量 Momentum Transformer 在長期市場中的整體表現。
  - **近期市場（2015–2020）**：測試 Momentum Transformer 在市場不穩定時的適應能力（包括 2015 年中國股災、2018 年股市波動等）。
  - **SARS-CoV-2（COVID-19）市場危機（2020）**：測試 Momentum Transformer 在市場崩潰與復甦期間的表現。

**4. 可解釋性分析（Interpretability Analysis）**
- **變數重要性分析（Variable Importance）**：
  - 透過 **VSN（Variable Selection Network）** 評估 Momentum Transformer 在不同市場條件下的決策機制。
  - 量化不同市場特徵（短期 vs. 長期動量、MACD、變化點指標）的相對影響力。

- **注意力機制分析（Attention Visualization）**：
  - 可視化 Momentum Transformer 的多頭注意力權重，解析模型如何根據歷史市場變動做出交易決策。
  - 研究其對市場轉折點（momentum turning points）的關注程度。

**5. 交易成本分析**
- **模擬不同交易成本（C）對策略績效的影響**：
  - 設定 C = 0 到 3bps（基點），計算扣除交易成本後的夏普比率變化。
  - **對比不同模型（LSTM、Transformer、Momentum Transformer）在交易成本下的表現**：
    - **LSTM 受到交易成本影響最大**，因為它更依賴短期交易。
    - **Momentum Transformer 由於較長的交易信號持續時間，受交易成本影響較小**。

**6. 模型訓練與超參數調整**
- **優化方法**：
  - 搭配 **Adam Optimizer** 進行梯度下降（Stochastic Gradient Descent, SGD）。
  - 直接優化夏普比率作為損失函數（Sharpe Loss Function）。
  - 早停（Early Stopping）機制防止過擬合。

- **超參數調整（Hyperparameter Tuning）**：
  - **網格搜索（Grid Search）+ 隨機搜索（Random Search）**。
  - 針對不同 Transformer 變體（Momentum Transformer、Informer、Convolutional Transformer）進行最優超參數尋找。

**總結**

本研究採用了綜合方法驗證 Momentum Transformer 的有效性：
1. **基於 Transformer 設計一種新型 Momentum 交易策略**，並與傳統方法（LSTM、TSMOM）進行對比。
2. **使用歷史期貨數據（1990–2020）進行回測**，檢測模型在不同市場環境下的適應性與穩健性。
3. **分析可解釋性**，透過注意力機制與變數選擇網絡來解析 Momentum Transformer 如何做出交易決策。
4. **考慮交易成本的影響**，確保模型的實際應用價值。

這種方法論有助於檢驗 Momentum Transformer 是否能在量化交易領域提供更優越的交易信號，同時保持較高的可解釋性與實用性。


<a name="S4"></a>
## 4. **研究結果**

**1. Momentum Transformer 相較於基準模型的表現**
Momentum Transformer 透過 Transformer 的注意力機制，克服 LSTM 在長期記憶與市場 regime 變化時的缺陷，表現顯著提升：
- 與 LSTM 相比，Momentum Transformer **夏普比率（Sharpe Ratio）提升 50%**（1995-2020），在 2015-2020 期間則提升 **109%**。
- 在 2015-2020 年的市場非平穩（non-stationary）期間，Momentum Transformer 仍能維持穩定獲利。
- 在 SARS-CoV-2 市場崩盤與復甦期間，Momentum Transformer 相較於其他 Transformer 架構表現更為穩健。

**2. 解釋能力與市場適應性**
Momentum Transformer 透過注意力機制，使交易決策更具解釋性：
- 注意力權重圖顯示，模型可自動識別**市場 regime 變化**，例如 SARS-CoV-2 危機時的**市場崩盤與牛市轉折點**。
- **變數重要性分析** 顯示，模型能夠根據不同市場條件，自適應地調整動能與均值回歸策略的組合。
- **結合變點檢測（CPD）**，Momentum Transformer 可識別市場 regime 轉變，進一步提升交易決策的穩健性。

**3. 交易成本影響分析**
Momentum Transformer 在考慮交易成本後仍能維持穩定表現：
- **在 2015-2020 期間，考慮 3bps 交易成本後，Momentum Transformer 仍能維持正向報酬**，相較於 LSTM，其表現衰退幅度較小。
- Momentum Transformer 主要受益於**長期趨勢識別能力**，避免頻繁交易帶來的成本影響。
- 在商品期貨（Commodities）交易方面，Momentum Transformer 即使在交易成本達 3bps 時，仍能維持 **1.23** 的夏普比率。


<a name="S5"></a>
## 5. **研究結論**

該研究介紹了一種基於注意力機制的深度學習架構——**Momentum Transformer**，並將其應用於時間序列動量交易策略。以下是主要的研究結論：

1. **Momentum Transformer 在風險調整後表現優於傳統與深度學習基準策略**
   - 相較於 LSTM（Long Short-Term Memory）架構的深度動量網絡（Deep Momentum Network, DMN），Momentum Transformer 在 1995–2020 年的回測中，夏普比率（Sharpe Ratio）提升了 50%，2015–2020 年的提升更達 109%。
   - 該模型不僅能提高收益，還能降低交易風險指標（如波動性、最大回撤），並且能更準確地預測價格變動方向。

2. **具備強大的長期依賴學習能力**
   - 相較於 LSTM，Momentum Transformer 能學習更長時間跨度的市場模式。適用的一年輸入窗口（sequence length = 252）比 LSTM 傳統的 63 天窗口更有效，能捕捉更長期的市場趨勢。

3. **對市場環境變化的適應性更強**
   - Momentum Transformer 能夠自適應市場新政權（market regime），例如在 SARS-CoV-2（COVID-19）市場崩盤期間表現出色，相比於 LSTM 更能應對市場衝擊並抓住隨後的牛市趨勢。
   - 通過多頭注意力機制（Multi-Head Attention），模型能夠同時關注不同時間尺度的市場行為，提高對市場轉折點的識別能力。

4. **加入變化點檢測（Change Point Detection, CPD）能進一步提升表現**
   - 在 2015–2020 年期間，加入 CPD 模組後，Momentum Transformer 的夏普比率進一步提升 17%。
   - CPD 幫助模型更好地識別市場政權變化，提高市場轉折點（momentum turning points）的判斷能力。

5. **相較於其他 Transformer 架構，Momentum Transformer 具有較高的穩健性**
   - 在回測中，Momentum Transformer 在不同市場條件下都能維持穩定的高夏普比率，而其他 Transformer 變體（如 Informer、Convolutional Transformer）雖然在特定時間段內表現良好，但整體穩定性較差。

6. **模型具備較好的可解釋性（Interpretability）**
   - 透過**變數選擇網絡（Variable Selection Network, VSN）**，Momentum Transformer 能夠識別哪些市場指標在不同時期最具影響力，例如在市場崩盤期間，短期動量因子權重上升，而長期因子則在市場趨勢穩定後變得更重要。
   - **注意力機制（Attention Mechanism）提供市場趨勢劃分能力**，幫助識別市場的政權變化與重要事件的影響，進一步提升模型決策的透明度。

7. **交易成本的影響相對較小**
   - 研究顯示，傳統 LSTM 架構在交易成本考慮後的績效下降幅度較大，而 Momentum Transformer 由於較少依賴高頻交易，受交易成本影響較小，在 C = 3bps（基點）時仍能維持合理的風險調整後收益。

**結論**

Momentum Transformer 成功整合了 LSTM 的局部模式學習能力與 Transformer 的長期依賴學習能力，在動量交易策略中展現出顯著優勢。該模型能夠：
- 提供更穩定且優越的風險調整後收益；
- 在市場極端事件（如 COVID-19 市場崩盤）期間表現優異；
- 具備較好的可解釋性，有助於理解模型如何決策；
- 在交易成本考量下仍保持競爭力。

未來研究可以進一步探索該模型在股票市場、不同資產類別，以及納入其他因子（如價值、品質因子）的應用。