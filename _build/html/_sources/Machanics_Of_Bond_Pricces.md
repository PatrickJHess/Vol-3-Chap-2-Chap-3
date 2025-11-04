


## <span style="font-family:Franklin Gothic Medium', sans-serif;">The Mechanics Of Bond Pricing</span>



This chapter introduces essential date manipulation skills for finance professionals. Several new functions are developed. The most important of these is accrued\_interest().  Bonds are quoted without accrued interest ('clean') but trade with accrued interest ('dirty').  It's fair to characterize the calculation of accrued interest as messy.  Here we demonstrate the concepts and calculations.  No need to memorize the details: the goal is a thorough understanding of concepts.  accrued\_interest()  calculates accrued interest for government and non-government bonds (e.g. corporate and agencies). Some of the mess is the difference in the calculations for government and non-government bonds.  The function handles this and other details.

### Bond Prices And Accrued Interest

The transaction price (or dirty price) of a coupon bond is the sum of its quoted (or clean) price and accrued interest. Accrued interest is the allocation of a coupon payment between payment dates. It's worth noting that accrued interest determines how taxable interest income is allocated between purchasers and sellers of a bond.

For government notes and bonds, accrued interest is calculated based on the actual number of days from the last coupon payment relative to the total days between payments: the so-called actual/actual rule. For non-government bonds, a 30-day month is assumed for accrued interest calculations: the so-called 30/360 rule.

### Illustrating Accrued Interest With Five Maturity Dates

Two time periods are required to calculate accrued interest:

1. the time remaining until the next payment,  
2. the time between the next and previous payments.

Until it matures, a coupon bond makes a payment every year on the anniversary of its maturity date. If the maturity date is a month-end, all payments are as well.  Consider a bond maturing on April 30$^{th}$ making semi-annual coupon payments. Before April 30$^{th}$ of the current year, the next payment date will be April 30$^{th}$ in the current year and the previous payment date is October 31$^{st}$ of the previous year .After April 30$^{th}$ and before October 31$^{st}$ of the current year, the next payment occurs on October 31$^{st}$.

Since May of 2024 bond trades settle one business day following the trade date.  Accrued interest is calculated relative to the settlement date.   The module datetime is part of the standard Python library and manipulates dates.  We use it extensively in this and other chapters.  Two other modules are also needed.: dateutil and  the built-in module calendar.  The next section of the chapter, the notebooks *Dealing With Dates*, illustrates the uses of datetime, dateutil,  and calendar.  A more general discussion is provided in [A Quick Introduction To Manipulating Dates](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/Manipulating_Dates.html#a-quick-introduction-to-manipulating-dates). 

Five maturity dates are selected to illustrate the calculations. The fifth bond matures on February 29$^{th}$ in a leap year.  The current settlement date is January 21$^{st}$ 2025 and February 29$^{th}$ doesn't exist in 2025\.  Controlling for month-end, however, will automatically adjust the coupon payment date to February 28 in 2025\.

* February 28$^{th}$ 2025  
* July 15$^{th}$ 2025  
* August 31$^{st}$ 2025  
* January 15$^{th}$ 2026  
* February 29$^{th}$ 2028
### The Next Coupon Period

The end of the next coupon period is determined by adding the number of months between payments to the settlement date.  In these examples the bonds pay semi-annually and the number of months between payments is six

### Determining The Next Coupon Date

Government notes and bonds make semi-annual payments.  When a coupon bond is purchased, the next coupon payment date will be within six months of the settlement date.  
In this example the settlement date is January 21$^{st}$ 2025 making the next coupon date falling between January 21$^{st}$ 2025 and July 21$^{st}$ 2025\. If the maturity month and day of the security is between January 21$^{st}$ and July 21$^{st}$, the next coupon payment date will be the maturity month and day in 2025\. The exception to this is the bond that matures on February 29$^{th}$ 2028\. Because of the month-end maturity, its next coupon date is adjusted to February 28$^{th}$ 2025\.


<img src='https://docs.google.com/drawings/d/e/2PACX-1vS1L8ZT3QiCyUdLd8kddTgsgqGHUp7u8d1nUDZ4KhiIMTuHrPq1Jc3dpfmSmgbaI6bd4EPLnTqEKJj4/pub?w=960&h=720'>

. 

### Calculating Accrued Interest

Accrued interest for Government bonds is calculated by determining the ratio of days since the last coupon payment to the total days between coupon payments. This calculation uses the settlement date, next coupon date, and last coupon date. For Corporate and other bonds, accrued interest is calculated based on a 30-day month and 360-day year.  Using the settlement date of January  21$^{st}$ 2025, the diagram highlights the calculations for the five Government bonds paying a coupon on February 28$^{th}$ 2025 or July 15$^{th}$ 2025\.

<img src='https://docs.google.com/drawings/d/e/2PACX-1vR6XvDjt0b_IiI23LnhIthZ1uMpS4dMOX9LH0gW5wMK_7DnpkaFiu1lkP3T8otpurLPU5jI9y8f18ea/pub?w=960&h=720'>

