# Simple wash trade detection

Author: [richardwu](https://github.com/richardwu).

Presented by: [Tensor](https://www.tensor.trade) - fastest NFT marketplace and aggregator on Solana

Under `notebooks/wash-trade-detection.ipynb`, you'll find an analysis of Solana NFT sales from 2022/09 to 2023/03 and simple heuristics to detect wash trading and suspicious trades.

## Data

You must download the marketplace dump file (1.5GB compressed) to `data/` from [Shadow Drive](https://www.shadow.storage/):
```sh
wget https://download.sdrive.app/file/b00d1afaee62e8c9acf171d5d20e6ce5 -O 20230301_marketplace_txs_w_rarity.csv.gz
# Check shasum
shasum 20230301_marketplace_txs_w_rarity.csv.gz
# > fcb1e67626874e1b3bd0d5b902b52d4f29c585b6  /Users/richardwu/Downloads/20230301_marketplace_txs_w_rarity.csv.gz
# Unzip + move to data folder.
gunzip 20230301_marketplace_txs_w_rarity.csv.gz
mv 20230301_marketplace_txs_w_rarity.csv data/
```
