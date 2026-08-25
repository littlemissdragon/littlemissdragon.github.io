---
layout: article
title: When they print money, what happens to your money
custom_css: article.css
include_mathjax: true
publish: true
---

## 1. Introduction ##

In La Casa de Papel, the Professor’s masterstroke isn't just stealing €2.4 billion—it’s printing billions more. As the gang throws cash from the Royal Mint, the public cheers. It feels like justice, like wealth redistributed to the common man. I cheered too.

But then I learned about inflation. That thrilling scene stopped feeling like justice and started feeling like a heist — not against the bank, but against the average people. Because when you print money without creating new value, you don't create wealth. You silently steal it from everyone who holds cash.

In this article, we want to discuss how printing money affects our cash.

First, we need to understand what money actually is.


## 2. Fiat money ##

Before we can understand why printing money is dangerous, we need to strip money down to its simplest form. Money is not wealth. Wealth is the resources you use to produce things and services. Money is just a token, a convenient IOU, that represents a claim on that wealth.

In the old days, you could take that paper IOU to the bank and exchange it for physical gold (a "gold certificate"). Today, the dollar is fiat money, which means it is backed by nothing physical. It is backed only by the government's promise and everyone's collective belief in that authority.

Three mechanisms hold the fiat money up:

+ Legal Tender Laws: The government declares: "This paper is legal tender for all debts, public and private." 

+ Tax Backing: The government demands that you pay your taxes only in its fiat currency.

+ Social Trust: Taxes and laws force you to acquire the money, but they don't force you to hold it. You hold it because you trust that your landlord, your grocery store, and your employer will accept it tomorrow. It is a self-fulfilling prophecy. 

Then what are the differences between fiat money and gold certificate?

## Fiat Money Vs. Gold ##

To understand the difference between fiat money and gold, we first need to understand the Equation of Exchange:

$$M × V = P × Q$$


Where:

+ $M$ = Money supply (total currency in circulation)

+ $V$ = Velocity of money (the rate of money being spent)

+ $P$ = Price level (average price of all goods)

+ $Q$ = The total quantity of goods and services produced

The left side (M × V) is the total amount of money changing hands in a year; The right side (P × Q)is the total value of all goods and services sold in that year. The total amount of money spent in the economy must exactly equal the total price of everything bought. Rearranging the equation to solve for the price level gives us:


$$P=\frac{M x V}{Q}$$

This shows us the critical difference between gold and fiat money:

+ Gold Standard: If $Q$ grows 5%, but $M$ (gold supply) stays the same, prices drop, i.e. **deflation**, as shown in Figure 1. Deflation encourages people to hoard cash, which lowers V (spending rate), which kills jobs, which causes depressions.

+ Fiat System: If $Q$ grows 5%, to keep $P$ from lowering, the government can increase the money supply ($M$) exactly as fast as the economy grows (or even faster), as shown in Figure 2. This allows them to prevent deflation. But if the government overprinted money, it would lead M growth to outpace Q growth, resulting in P growth, i.e. **inflation**, which is what often happens.



```python
import matplotlib.pyplot as plt
import numpy as np


fig_count = 1

# Set the style to a dark theme
plt.style.use("dark_background")

# Match website background
plt.rcParams["figure.facecolor"] = "#181818"
plt.rcParams["axes.facecolor"] = "#181818"
plt.rcParams["axes.edgecolor"] = "#181818"

# Create figure
fig, ax = plt.subplots(figsize=(8, 6))


# Data: Q ranges from 90 to 120
Q_range = np.linspace(90, 120, 100)
M_fixed = 100
V_stable = 1.0

# Price level must satisfy: P = (M * V) / Q
P_range = (M_fixed * V_stable) / Q_range

# Plot the curve
ax.plot(Q_range, P_range, 'b-', linewidth=2.5, label='P = (M × V) / Q')

# Mark Year 1 and Year 2
Q1, P1 = 100, 1.00
Q2, P2 = 105, 0.952

ax.scatter([Q1, Q2], [P1, P2], color='red', s=120, zorder=5, label='Equilibrium points')

# Annotate the points
ax.annotate(f'Year 1: Q={Q1}, P={P1:.2f}', 
            xy=(Q1, P1), xytext=(Q1 + 1.5, P1 + 0.02),
            fontsize=11, fontweight='bold', color='yellow')

ax.annotate(f'Year 2: Q={Q2}, P={P2:.3f}', 
            xy=(Q2, P2), xytext=(Q2 + 1.5, P2 - 0.03),
            fontsize=11, fontweight='bold', color='yellow')

# Add dashed reference lines
ax.axhline(y=1.0, color='gray', linestyle='--', alpha=0.5, linewidth=1)
ax.axvline(x=100, color='gray', linestyle='--', alpha=0.5, linewidth=1)

# Add an arrow showing the movement from Year 1 to Year 2
ax.annotate('', xy=(Q2, P2), xytext=(Q1, P1),
            arrowprops=dict(arrowstyle='->', color='pink', lw=2))

# Labels and title
ax.set_xlabel('Real GDP (Q) - Quantity of Goods Produced', fontsize=11)
ax.set_ylabel('Price Level (P)', fontsize=11)

# Set axis limits
ax.set_xlim(90, 120)
ax.set_ylim(0.80, 1.15)

# Grid and legend
ax.grid(alpha=0.3, linestyle='--')
ax.legend(loc='upper right', fontsize=11)

# Add a text box explaining the mechanics
props = dict(boxstyle='round,pad=0.5', facecolor='wheat', alpha=0.25, edgecolor='brown')
text_str = (f'M × V = {M_fixed} × {V_stable} = 100 (constant)\n'
            f'P × Q = 100 (must remain equal)\n\n'
            f'Year 1: 1.00 × 100 = 100\n'
            f'Year 2: 0.952 × 105 = 100')
ax.text(111, 1.0, text_str, fontsize=10, verticalalignment='top', bbox=props)

# Add a second annotation showing the "5% drop" visually
ax.annotate('Price drops ~4.8%', 
            xy=(102.5, 0.976), xytext=(102.5, 0.90),
            arrowprops=dict(arrowstyle='<->', color='yellow', lw=1.5),
            fontsize=10, color='yellow', ha='center')

ax.annotate('GDP grows 5%', 
            xy=(102.5, 0.95), xytext=(102.5, 1.08),
            arrowprops=dict(arrowstyle='<->', color='pink', lw=1.5),
            fontsize=10, color='pink', ha='center')

# Suptitle (moved up so it's visible - y=0.0001 was pushing it off screen)
fig.suptitle(
    f"Figure {fig_count}. Gold Standard: When Q Rises 5%, P Must Fall ~5%\n(M × V is Fixed at 100)",
    fontsize=12,
    color='white',
    y=0.0001
)


# Increment counter (won't persist after script ends, but kept for logic)
fig_count += 1

plt.tight_layout()
plt.show()
```


    
![png](/assets/images/2026-08-12-when-they-print-money-what-happens-to-your-money_files/2026-08-12-when-they-print-money-what-happens-to-your-money_3_0.png)
    


```python
# plot the fiat system: when Q increases, V and P stay the same, what happens to M
# Create the figure
fig, ax = plt.subplots(figsize=(8, 6))

# Range of possible Q values (90 to 120)
Q_range = np.linspace(90, 120, 100)
V = 1.0

# Fiat system: M tracks Q exactly to keep P = 1.0
M_fiat = Q_range  # M equals Q

# Gold standard: M is fixed
M_gold = np.ones_like(Q_range) * 100

# Plot both
ax.plot(Q_range, M_fiat, color='yellow', linewidth=2.5, label='Fiat System: M tracks Q (+5% expansion)')
ax.plot(Q_range, M_gold, color='lightgreen', linewidth=2.5, label='Gold Standard: M fixed at 100')

# Mark the 5% growth point
ax.scatter([100, 105], [100, 105], color='red', s=120, zorder=5)
ax.annotate('Year 1: Q=100, M=100', xy=(100, 100), xytext=(92, 102),
            fontsize=10, fontweight='bold', color='yellow')
ax.annotate('Year 2: Q=105, M=105', xy=(105, 105), xytext=(95, 107),
            fontsize=10, fontweight='bold', color='yellow')


# Labels and title
ax.set_xlabel('Real GDP (Q) - Quantity of Goods', fontsize=11)
ax.set_ylabel('Money Supply (M)', fontsize=11)


# Set axis limits
ax.set_xlim(90, 120)
ax.set_ylim(90, 115)

# Grid and legend
ax.grid(alpha=0.3, linestyle='--')
ax.legend(fontsize=11, loc='upper left')

# Add annotation showing the 5% expansion
ax.annotate('+5% expansion in M', xy=(105, 105), xytext=(102, 110),
            arrowprops=dict(arrowstyle='->', color='yellow', lw=2),
            fontsize=10, color='yellow')

ax.annotate('+5% growth in Q', xy=(105, 105), xytext=(105, 101),
            arrowprops=dict(arrowstyle='->', color='pink', lw=2),
            fontsize=10, color='pink')

# Add a text box
props = dict(boxstyle='round,pad=0.5', facecolor='yellow', alpha=0.2, edgecolor='yellow')
text_str = (f'P = (M × V) / Q = 1.00 (constant)\n'
            f'M = Q × P = Q (since P=1, V=1)\n\n'
            f'When Q grows 5%, M must grow 5%\n'
            f'to maintain price stability.')
ax.text(105, 92, text_str, fontsize=9, verticalalignment='bottom', bbox=props)

# Suptitle (moved up so it's visible - y=0.0001 was pushing it off screen)
fig.suptitle(
    f"Figure {fig_count}.Fiat System: M Expands Proportionally to Q)",
    fontsize=12,
    color='white',
    y=0.0001
)


# Increment counter (won't persist after script ends, but kept for logic)
fig_count += 1
plt.tight_layout()
plt.show()
```


    
![png](/assets/images/2026-08-12-when-they-print-money-what-happens-to-your-money_files/2026-08-12-when-they-print-money-what-happens-to-your-money_4_0.png)
    


## The Unescapable Inflation ##

In theory, a well-managed fiat system keeps prices stable by expanding the money supply ($M$) at the same rate as economic growth ($Q$). In practice, this perfect alignment rarely occurs. Due to GDP forecast errors, unexpected economic shocks, political over-expansion, or the innate imprecision of the monetary transmission mechanism, $M$ often grows faster than $Q$. When this happens, the price level ($P$) rises, and that rise is what we call **inflation**.

Now, let's see how printing money can cause price level to rise. Economists make two assumptions:

+ $V$ is stable (people's spending habits don't change much in the short run).

+ $Q$ is fixed (the economy produces at full capacity in the short run).

If V and Q are constant, the equation simplifies to:

$$
P \propto M
$$

Prices are directly proportional to the money supply, as shown in Figure 3. 

Why doesn't $Q$ increase?

A common misunderstanding is that printing money creates wealth, or more money means more goods. The figure corrects this error. The real productive capacity includes factories, workers, and raw materials. Printing money does not build factories or train workers. It only creates claims on existing goods. If the new money is used for productive investment, $Q$ may increase over time. But in the short run—or if the money is spent on consumption rather than investment. The increased $M$ then translates directly into price increases.

**Inflation is not when things get more expensive. It is when money gets less valuable.** Cash savers, pensioners on fixed incomes, and workers with stagnant wages see their purchasing power erode. Meanwhile, debtors see their real debt burden shrink. The price increase is not a natural phenomenon; it is the mechanical result of $M$ growing faster than $Q$.

Printing money inevitably creates **inflationary** pressure. Instead of fighting it, the government embraces a low, steady inflation rate (2%) because:

+ It gives the central bank room to cut rates below 0% (in real terms) during recessions.

+ It slowly erodes the real value of government debt.

+ It allows companies to cut real wages without triggering worker backlash.

The system becomes self-reinforcing: The existence of fiat money requires inflation to function smoothly, and the existence of controlled inflation validates the need for fiat money. This leads to a harsh reality that:

Your cash will continue to lose its purchasing power.

```python
# ==============================================
# PLOT: P ∝ M (Proportional Relationship)
# ==============================================

# Fixed parameters
V = 2.0   # Velocity of money (constant)
Q = 10.0  # Real output (constant)

# Money supply range: 0 to 20 units
M = np.linspace(0, 20, 100)

# Calculate Price Level: P = (V/Q) × M
slope = V / Q
P = slope * M

# Create the plot
fig, ax = plt.subplots(figsize=(8, 6))

# Plot the proportional relationship
ax.plot(M, P, linewidth=3, color='lightgreen', label=f'P = ({V}/{Q}) × M = {slope:.2f} × M')

# Fill area under the curve
ax.fill_between(M, 0, P, alpha=0.15, color='blue')

# Add reference points showing the proportion
M_points = [0, 5, 10, 15, 20]
for m in M_points:
    p = slope * m
    ax.plot(m, p, 'ro', markersize=8)
    # Add dashed lines to axes
    ax.axvline(x=m, color='gray', linestyle='--', alpha=0.3, linewidth=1)
    ax.axhline(y=p, color='gray', linestyle='--', alpha=0.3, linewidth=1)
    # Annotate the point
    ax.annotate(f'({m}, {p:.1f})', 
                xy=(m, p), 
                xytext=(m-0.8, p+0.3),
                fontsize=10, color='darkred',
                bbox=dict(facecolor='white', edgecolor='none', alpha=0.7))

# Add origin annotation
ax.plot(0, 0, 'ro', markersize=8)

# Labels and title
ax.set_xlabel('Money Supply (M)', fontsize=14, fontweight='bold')
ax.set_ylabel('Price Level (P)', fontsize=14, fontweight='bold')

# Grid and legend
ax.grid(True, alpha=0.3)
ax.legend(loc='upper left', fontsize=12)

# Set axis limits
ax.set_xlim(-1, 21)
ax.set_ylim(-0.2, 4.5)
# Suptitle (moved up so it's visible - y=0.0001 was pushing it off screen)
fig.suptitle(
    f"Figure {fig_count}.P ∝ M: Price Level is Proportional to Money Supply",
    fontsize=12,
    color='white',
    y=0.0001
)


# Increment counter (won't persist after script ends, but kept for logic)
fig_count += 1


plt.tight_layout()
plt.show()


```


    
![png](/assets/images/2026-08-12-when-they-print-money-what-happens-to-your-money_files/2026-08-12-when-they-print-money-what-happens-to-your-money_6_0.png)
    


## What happens to your money when they print money ##

Let's calculate the real value of your money as inflation happens:

$$R_n = \frac{N}{(1 + \pi)^n}$$

Where:
- $n$ = Number of years
- $R$ = The real value of your money after n years
- $N$ = The nominal (face) value of your money (e.g., \$100,000)
- $\pi$ = Inflation rate (as a decimal, e.g., 0.05 for 5%)


One example is shown in Figure 4. If you have $100,000 in savings, and they print 5% more money every year:

+ $N$ = \$100,000
+ $R_{1}$ = \$100,000 / 1.05 = \$952,38.
+ $R_{2}$ = \$100,000 / 1.05 / 1.05 = \$90,909; etc.


Printing money transfers purchasing power from cash holders and fixed-income receivers to who prints it (which spends the new money first) and to debtors (who repay loans with cheaper dollars).

In La Casa de Papel, when the gang printed €2.4 billion in new, untraceable currency, the purchasing power from normal citizens was transferred to the gang, leaving the real value of other citizens' money to become:

$$
R = N \cdot \frac{M}{M + \Delta M}
$$

Where: 
+ $\Delta M$: New money printed, €2.4 billion

```python
# ==============================================
# PLOT: Cash Savings - Purchasing Power Erosion
# ==============================================

# Initial savings
initial_savings = 100000  # $100,000

# Money supply increase (inflation scenarios)
money_printing = np.array([0, 5, 10, 15, 20, 25])  # % increase in money supply

# Calculate real value of savings: Real = Nominal / (1 + inflation)
real_value = initial_savings / (1 + money_printing / 100)

# Calculate loss
loss = initial_savings - real_value

# Create the plot
fig, ax = plt.subplots(figsize=(8, 6))

# Plot the real value line
ax.plot(money_printing, real_value, linewidth=3, color='red', marker='o', markersize=10, 
       label='Real Value')

# Add horizontal line at original value
ax.axhline(y=initial_savings, color='yellow', linestyle='--', alpha=0.7, linewidth=2, 
           label='Original Value ($100,000)')

# Fill the loss area
ax.fill_between(money_printing, real_value, initial_savings, alpha=0.25, color='pink', 
                 label='Loss in Purchasing Power')

# Add value labels above each point
for i, (mp, rv) in enumerate(zip(money_printing, real_value)):
    ax.annotate(f'${rv:,.0f}', 
                xy=(mp, rv), 
                xytext=(mp-1.5, rv+2000),
                fontsize=9, color='darkred', fontweight='bold',
                bbox=dict(facecolor='white', edgecolor='none', alpha=0.8))


# Labels and title
ax.set_xlabel('Money Supply Increase (%)', fontsize=11, fontweight='bold')
ax.set_ylabel('Real Value of $100,000 Cash ($)', fontsize=11, fontweight='bold')

# Grid and legend
ax.grid(True, alpha=0.3)
ax.legend(loc='upper right', fontsize=10)

# Set axis limits
ax.set_xlim(-1, 26)
ax.set_ylim(70000, 115000)

# Suptitle (moved up so it's visible - y=0.0001 was pushing it off screen)
fig.suptitle(
    f"Figure {fig_count}.Cash Savings: Purchasing Power Erosion\nWhen More Money is Printed",
    fontsize=12,
    color='white',
    y=0.0001
)


# Increment counter (won't persist after script ends, but kept for logic)
fig_count += 1

plt.tight_layout()
plt.show()


```


    
![png](/assets/images/2026-08-12-when-they-print-money-what-happens-to-your-money_files/2026-08-12-when-they-print-money-what-happens-to-your-money_8_0.png)
    


## Conclusion ##

By understanding the fiat money system, we see how printing money inevitably causes inflation, which then erodes the purchasing power of cash over time. Due to the unavoidable reality of inflation, cash is not a long-term store of value, but only a short-term transaction tool.

To protect your wealth, you must convert your cash into productive assets—such as stocks, real estate, and businesses, that grow with the economy and outpace inflation. The system is structurally designed to penalize those who hold still and reward those who put their capital to work.
