# Financial Python

## **Volume: Basic Concepts of Fixed Income**

### **Chapters Two and Three: Accrued Interest and Bond Pay Data**

Chapter One of *Basic Concepts of Fixed Income* introduced the fundamentals of bond pricing and demonstrated how to calculate the term structure of interest rates using the prices of short-term U.S. Treasury Bills (those with a maturity of one year or less).

To significantly expand our knowledge of the term structure—and, consequently, gain a deeper understanding of the financial markets—we must extend this analysis using coupon bonds, which often have much longer maturity dates. This process is known as bootstrapping the term structure of interest rates.

Applying the bond pricing concepts from Chapter One to coupon bonds requires two specific pieces of information:

1. The price of the coupon bonds.  
2. The dates and amounts of all payments made by the coupon bonds.

With this data for a substantial number of bonds, we can use the present value principle to derive the present value factors—or "zero prices"—that determine the bonds' values. As established in Chapter One, the term structure of interest rates naturally follows from these zero prices.

To equip us with the necessary inputs, this book dedicates two subsequent chapters to these requirements:

1. **Chapter Two: *Accrued Interest*** focuses on a critical calculation needed to convert the quoted prices of coupon bonds into their actual transaction prices.  
2. **Chapter Three: *Bond Payment Data*** details the calculation of the payment dates and amounts for coupon bonds.

A candid note: The financial concepts of these two chapters are straightforward, the implementation in Python is more challenging. These chapters involve complex, fundamental work—the "blocking and tackling"—necessary for advanced analysis.
___

