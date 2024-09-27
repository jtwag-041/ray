# rar
**Risk-adjusted Bond Yield Calculator**

Creates a bond profile and calculates the bond yield, expected losses, and the risk-adjusted bond yield. Takes the following input from the user:

- The bond's ISIN number
- The issuer's sector
- The bond's next call date

The bond yield corresponds to the bond's Yield to Worst (YTW), which takes the minimum yield between the bond's Yield to Maturity (YTM) and Yield to Call (YTC)*. 

Yield to Maturity is calculated as follows:

((((bond coupon)/2)+(par value-bond price))/tenor**)/(((par value+bond price)/2)*2)

The formula to find the YTC is the same except the maturity date is replaced by the user-generated next call date.

Expected losses (EL) are calculated using the following formula:

EL = probability of default * exposure at default * loss given default, where

probability of default (PD) = the probability of default based on the bond's tenor, its rating, and the corresponding historical cumulative default rate**
exposure at default (EAD) = bond's purchase price  
loss given default (LGD) = 1 - recovery rate***


**Demo**


![runtointeractive_rar-ezgif com-speed (1)](https://github.com/user-attachments/assets/7cfc335a-42f3-4124-92df-5401ad88b525)

**Sources**

Oblible.com

Average recovery by sector, 1987-2023 for nonfinancial sectors, S&P Global Market Intelligence's CreditPro and S&P Global Ratings Credit Research & Insights

Global Corporate Average Cumulative Default Rates, 1981 - 2016, S&P Global Fixed Income Research and S&P CreditPro


**Notes**

* YTC takes the user-generated next call date as it may not always be displayed on Oblible.
** Tenor is equal to the maturity date minus the settlement date. The settlement date is set to April 3, 2024. S&P's Global Corporate Average Cumulative Default Rates is used as proxy to lookup the probability of default.
*** The calculator takes as input the selected sector and looks up the corresponding recovery rate on S&P's Average recovery rate by sector

Overview of Oblible's webpage

![image](https://github.com/user-attachments/assets/9647cd5a-ac97-41c6-8313-f45e3dbfd87a)
