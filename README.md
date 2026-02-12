
# Black-Scholes Visual Explainer
<img width="2968" height="1621" alt="Screenshot 2026-02-12 201557" src="https://github.com/user-attachments/assets/fa1dbf50-9bb3-4b78-9df6-2373ba9f27e7" />

<img width="2987" height="1670" alt="Screenshot 2026-02-12 201604" src="https://github.com/user-attachments/assets/79c37454-ca0b-4602-8ed9-9a3faf2ef24b" />

## Developer: tubakhxn


A fully interactive, visually impressive explainer for the Black-Scholes option pricing model, built with Streamlit, Plotly, NumPy, and SciPy.

## Features

- **Black-Scholes formula** for European Call and Put options
- **Greeks**: Delta, Gamma, Vega, Theta, Rho
- **Interactive sliders** for:
  - Stock price (S)
  - Strike price (K)
  - Volatility (σ)
  - Time to maturity (T)
  - Risk-free rate (r)
- **Real-time updating** of option price and Greeks
- **3D surface plot**: Stock Price vs Volatility vs Option Price
- **2D plot**: Delta vs Stock Price
- **Smooth animated transitions**
- **Professional dark theme** with sidebar controls, large price display, and colored Greek indicators

## Mathematical Formulas

Let $S$ = Stock price, $K$ = Strike price, $T$ = Time to maturity, $r$ = Risk-free rate, $\sigma$ = Volatility.

- $d_1 = \frac{\ln(S/K) + (r + 0.5\sigma^2)T}{\sigma\sqrt{T}}$
- $d_2 = d_1 - \sigma\sqrt{T}$

**Call Price:**
$$C = S N(d_1) - K e^{-rT} N(d_2)$$

**Put Price:**
$$P = K e^{-rT} N(-d_2) - S N(-d_1)$$

Where $N(x)$ is the cumulative distribution function of the standard normal distribution.

### Greeks

- **Delta:** $\frac{\partial C}{\partial S} = N(d_1)$ (Call), $N(d_1)-1$ (Put)
- **Gamma:** $\frac{\partial^2 C}{\partial S^2} = \frac{N'(d_1)}{S\sigma\sqrt{T}}$
- **Vega:** $\frac{\partial C}{\partial \sigma} = S N'(d_1) \sqrt{T}$
- **Theta:** $\frac{\partial C}{\partial T}$ (see code for full formula)
- **Rho:** $\frac{\partial C}{\partial r}$ (see code for full formula)

## Usage

1. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the app:
   ```bash
   streamlit run app.py
   ```

## File Structure
- `app.py` — Streamlit app UI and visualization
- `black_scholes.py` — Pricing and Greeks functions
- `requirements.txt` — Dependencies
- `README.md` — This file

---


**Enjoy exploring the Black-Scholes model interactively!**

---

## How to Fork

1. Click the **Fork** button on the top right of this repository (on GitHub).
2. Clone your forked repo:
   ```bash
   git clone https://github.com/your-username/Black-Scholes-Visual-Explainer.git
   ```
3. Install dependencies and start developing!

---

**Made by tubakhxn**

