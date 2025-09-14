
# Option Strategy Payoff Plotter 📈

This repository contains a **Python + Plotly** function to generate interactive payoff diagrams for multi-leg option strategies.  
It is designed for traders, analysts, and risk managers who want to quickly visualize **profit and loss across different stock price scenarios**.

---

## ✨ Features
- Supports **calls, puts, and stock legs**
- Handles both **long** and **short** positions
- Built with **Plotly** for interactive visualization
- Adds breakeven lines and current spot price markers
- Flexible for single strategies or multi-leg combinations (e.g. straddles, strangles, butterflies, covered calls)

---

## 🚀 Usage Example

### Covered Call
```python
plot_option_strategy_plotly(
    legs=[
        {'type': 'call', 'strike': 200, 'position': 'short', 'premium': 0.66, 'stock_buying_price':0, 'derivative_type':'option'},
        {'type': 'call', 'strike': 0, 'position': 'long', 'premium': 0, 'stock_buying_price':195, 'derivative_type':'stock'}
    ],
    spot_price=195,
    contracts=1
)

plot_option_strategy_plotly(
    legs=[
        {'type': 'call', 'strike': 180, 'position': 'long', 'premium': 8.50, 'stock_buying_price':0, 'derivative_type':'option'},
        {'type': 'call', 'strike': 190, 'position': 'short', 'premium': 4.25, 'stock_buying_price':0, 'derivative_type':'option'},
        {'type': 'call', 'strike': 190, 'position': 'short', 'premium': 4.25, 'stock_buying_price':0, 'derivative_type':'option'},
        {'type': 'call', 'strike': 200, 'position': 'long', 'premium': 1.20, 'stock_buying_price':0, 'derivative_type':'option'},
    ],
    spot_price=190
)