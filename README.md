# Retail Margin & Elasticity Stress Test: Commercial FP&A Simulation

## Executive Summary
Wholesale supply chain inflation forces retail finance leadership to decide between:
1. **Absorbing cost inflation** to protect volume, causing immediate gross margin compression.
2. **Passing through cost increases**, which risks demand destruction depending on category price elasticity (β).

This project combines econometric demand estimation (β = %ΔQ / %ΔP) with dynamic financial scenario modeling (+5%, +10%, +15% cost inflation) to evaluate category profitability under **Absorb Cost** vs. **Pass-Through** strategies.

## 1. Econometric Price Elasticity Estimation (β)

Using a log-log Ordinary Least Squares (OLS) specification:

> **ln(Quantityₜ) = α + β · ln(Priceₜ) + εₜ**

Where β directly reflects the price elasticity of demand (%ΔQ / %ΔP). Categories are classified into three commercial tiers:
* **Inelastic / Pricing Power** (-1.0 < β < 0): Volume drops less than price rises.
* **Elastic / High Risk** (β ≤ -1.0): Volume loss exceeds price gains.
* **Positive / Other** (β > 0): Potential premium mix or trend-distorted categories.

## 2. Financial Simulation: Absorbing Cost vs. Passing Through Inflation

We model three inflation shock levels (+5%, +10%, +15%) applied to wholesale unit costs (baseline COGS = 60% of retail price) across two core commercial strategies:
1. **Absorb Cost (Hold Price):** Protect volume, accept margin erosion.
2. **Pass-Through Inflation:** Increase unit price proportionally, absorb elasticity-driven volume drop.

## 3. Executive FP&A Recommendations

1. **Selective Pass-Through Policy:** Fully pass through wholesale inflation on inelastic staples (`health_beauty`, `watches_gifts`, `perfumery`). Margin expansion in these categories outweighs minor volume softening.
2. **Elastic Shock Containment:** Freeze prices on `consoles_games` (β ≈ -2.28). Passing through cost inflation triggers demand collapse, worsening net margin impact. Wholesale cost pressures here must be handled via vendor renegotiation or supplier rebates.
3. **Audit Positive-Beta Segments:** Categories like `bed_bath_table` and `computers_accessories` exhibit non-negative empirical betas, reflecting premium product-mix trends rather than genuine pricing insensitivity. Break these down to the SKU level before taking price actions.
