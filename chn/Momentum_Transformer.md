[TOC]

# Trading with the Momentum Transformer: An Intelligent and Interpretable Architecture

## 1. **摘要**

本研究提出了一種基於注意力機制的深度學習架構——**Momentum Transformer**，用於時間序列動量交易策略。我們的方法結合了 Transformer 的全局時間依賴性學習能力與 LSTM（Long Short-Term Memory）的局部模式識別能力，以提升交易決策的準確性和穩健性。 

相較於傳統的 LSTM 架構與基準動量策略，Momentum Transformer 顯示出顯著的性能提升，尤其在市場環境變化（regime change）期間仍能保持卓越表現。該模型透過多頭注意力機制（Multi-Head Attention）學習市場在不同時間尺度上的模式變化，並利用可解釋性網絡（Variable Selection Network, VSN）識別最重要的市場特徵。回測結果表明，Momentum Transformer 在 1995–2020 年期間的風險調整後收益（夏普比率）相較於 LSTM 提升 50%，而在 2015–2020 年市場非平穩時期的提升幅度更達 109%。此外，在 SARS-CoV-2（COVID-19）市場崩盤期間，Momentum Transformer 能夠迅速適應市場轉折，捕捉新趨勢，展現出優異的市場適應能力。

透過引入變化點檢測（Change Point Detection, CPD）模組，我們進一步提升了 Momentum Transformer 的表現，使其在市場 regime 轉變時更加靈活。同時，我們發現 Momentum Transformer 對交易成本較不敏感，即便在較高的交易成本環境下仍能保持穩定的回報表現。

總結而言，Momentum Transformer 透過結合深度學習技術與可解釋性機制，提供了一種更智能、更穩健的動量交易策略，並在市場極端環境下保持競爭力。我們的研究為量化金融中的深度學習應用提供了新的視角，未來可進一步擴展至股票市場、跨資產交易及其他因子驅動的投資策略。

## 2. **研究角度**

## 3. **研究方法**

## 4. **研究結論**

### **文獻總結：Momentum Transformer 的結論**

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