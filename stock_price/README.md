```python
import yfinance as yf
from matplotlib import pyplot as plt

NUM_DAYS = 60
STOCK_SYMBOL = 'GOOG'


def main():
    stock = yf.Ticker(STOCK_SYMBOL)
    stock_data = stock.history(period=f'{NUM_DAYS}d')
    stock_data['Open'].plot()

    plt.title(f'{STOCK_SYMBOL} Price in the Last {NUM_DAYS} Days')
    plt.show()


if __name__ == '__main__':
    main()

```
