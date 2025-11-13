


# The Mechanics Of Bond Pricing



This chapter focuses on essential date manipulation skills for finance professionals, introducing several new functions. The most significant is <font color='green'>'accrued_interest()</font>.   Accrued interest calculations are often complex, but understanding the concepts is crucial. Although bonds are quoted 'clean' (without accrued interest), they trade 'dirty' (with accrued interest). The purpose here is to thoroughly demonstrate the concepts and calculations, not to require memorizing every detail.


## Bond Prices And Accrued Interest

The transaction price (or dirty price) of a coupon bond is the sum of its quoted (or clean) price and accrued interest. Accrued interest is the allocation of a coupon payment between payment dates. It's worth noting that accrued interest determines how taxable interest income is allocated between purchasers and sellers of a bond.

### Illustrating Accrued Interest With Five Maturity Dates

Two time periods are required to calculate accrued interest:

1. the time since the last scheduled payment,  
2. the time between the next and previous scheduled payments.

Until it matures, a coupon bond has a scheduled payment every year on the anniversary of its maturity date. If the maturity date is a month-end, all payments are as well.  Consider a bond maturing on April 30$^{th}$ making semi-annual coupon payments. Before April 30$^{th}$ of the current year, the next scheduled payment is April 30$^{th}$ in the current year and the previous scheduled payment is October 31$^{st}$ of the previous year. After April 30$^{th}$ and before October 31$^{st}$ of the current year, the next scheduled payment is October 31$^{st}$.

Because the purchaser of a bond owns it on the settlement date, the accrued interest does not include the settlement date. Five bonds paying semi-annual coupon payments are used to illustrate the concepts. The maturity dates of the bonds are:

* February 28$^{th}$ 2025  
* July 15$^{th}$ 2025  
* August 31$^{st}$ 2025  
* January 15$^{th}$ 2026  
* February 29$^{th}$ 2028

#### The Next Coupon Period

The end of the next coupon period is determined by adding the number of months between payments to the settlement date.  In these examples the bonds pay semi-annually and the number of months between payments is six. The settlement date is assumed to be January 21$^{st}$ 2025 . The next scheduled payment date of any semi-annual bond  is no later than  July 21$^{st}$ 2025\. If the maturity month and day of the bond is before July 21$^{st}$, the next scheduled payment is in the maturity month. For example, the bond maturing on February 29$^{th}$ 2028 follows the month-end rule, and the next shecduled payment is the last day of February 2025- the 28$^{th}$.

<img src='https://docs.google.com/drawings/d/e/2PACX-1vS1L8ZT3QiCyUdLd8kddTgsgqGHUp7u8d1nUDZ4KhiIMTuHrPq1Jc3dpfmSmgbaI6bd4EPLnTqEKJj4/pub?w=960&h=720'>

#### Calculating Accrued Interest
Accrued interest for Government bonds is calculated by determining the ratio of days since the last scheduled payment to the total days between the last and the next scheduled payments. The example below uses the so-called actual/actual day-count convention of Government bonds.  

<img src='https://docs.google.com/drawings/d/e/2PACX-1vR6XvDjt0b_IiI23LnhIthZ1uMpS4dMOX9LH0gW5wMK_7DnpkaFiu1lkP3T8otpurLPU5jI9y8f18ea/pub?w=960&h=720'>

Other securities use different day-count conventions; '30/360' is used for non-government bonds, 'Actual/360' is used for non-coupon bonds, and 'Actual/ 365' is used for some derivatives and international bonds and currency markets.  The Table *Day-Count Convention Rules* describes the four conventions.
' 
#### Day-Count Convention Rules
| Convention | Security Type | Amount | Accrued Day Ratio |
| :---- | :---- | :---- | :---- |
| **Actual/Actual** | Government Bonds. | Next Coupon | Numerator settlement less last payment date minus  1.Denominator actual number of days between next and last coupon payment dates,  |
| **30/360** | Corporate Bonds, Agency Bonds, and Mortgage-Backed Securities | Annual Coupon  | Numerator settlement less last payment date adjusting each month for 30 days minus  1\.  Denominator  360\. |
| **Actual/360** | Corporate loans, money-market, floating-rate notes. | Annual Coupon  | Numerator settlement less the last payment date minus  1\.   Denominator  360 |
| **Actual/365** | SWAPS and international bonds, and currency | Annual Coupont | Numerator settlement less the last payment date minus  1\.   Denominator is 365 |

The accrued interest formulas of each convention are shown in the Table *Day-Count Counvention Formulas*.
#### Day-Count Convention Formulas
|Day Count Convention | Accrued-Interest Formula |
| :---- | :---- |
| **Actual/Actual** |$Coupon\ Payment\times\large\frac{Actual\ Days\ Since\ Last\ Coupon\ Payment-1}{Actual\ Days\ Between\ Next\ And\ Last\ Coupon Payments}$|
| **30/360** | $Annual\ Coupon\ Payment\times\large\frac{(30/360)\ Days\ Since\ Last\ Coupon\ Payment-1}{360}$ |
| **Actual/360** |$Annual\ Coupon\ Payment\times\large\frac{Actual\ Days\ Since\ Last\ Coupon\ Payment-1}{360}$|
| **Actual/365** |$Annual\ Coupon\ Payment\times\large\frac{Actual\ Days\ Since\ Last\ Coupon\ Payment-1}{365}$|



### Bond Prices And Accrued Interest
The function <font color='green'>accrued_interest</font> developed in the notebook *Calculating Accrued Interest* of this chapter, accounts for the for conventions. As you undoubtedly surmised, the calculation requires the manipulation of dates and several Python modules are used in the notebook *Calculating Accrued Interest*.  If this is a new or somewhat unfamiliar subject, you should take a look at the notebook *Manipulating Dates* in this chapter as well as the notebook in the [background material](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/Manipulating_Dates.html).


