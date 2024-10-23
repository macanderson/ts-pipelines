```mermaid
%%{ init: { 'flowchart': { 'curve': 'monotoneX' } } }%%
graph LR;
trade_producer[fa:fa-rocket trade_producer &#8205] --> trades_topic{{ fa:fa-arrow-right-arrow-left trades_topic &#8205}}:::topic;
trades_topic{{ fa:fa-arrow-right-arrow-left trades_topic &#8205}}:::topic --> trade_to_ohlc[fa:fa-rocket trade_to_ohlc &#8205];
trade_to_ohlc[fa:fa-rocket trade_to_ohlc &#8205] --> ohlc_topic{{ fa:fa-arrow-right-arrow-left ohlc_topic &#8205}}:::topic;
streamlit-app[fa:fa-rocket streamlit-app &#8205]
ohlc_topic{{ fa:fa-arrow-right-arrow-left ohlc_topic &#8205}}:::topic --> ohlc_to_feature_store[fa:fa-rocket ohlc_to_feature_store &#8205];


classDef default font-size:110%;
classDef topic font-size:80%;
classDef topic fill:#3E89B3;
classDef topic stroke:#3E89B3;
classDef topic color:white;
```