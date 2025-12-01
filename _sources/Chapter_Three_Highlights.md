# Bond Payment Data

**Chapter Three of the Volume Basic Concepts of Fixed Income**.


**Key Topics Covered:**

* **Financial Concepts:**  
  * Settlement Dates  
  * Scheduled Payment Dates  
  * Actual Payment Dates  
* **Python Concepts:**  
  * NumPy arrays  
  * Python Series  
  * Accessing data with a URL address  
  * Custom modules

**Background Material:**

The examples and discussions in this chapter utilize the **datetime** and **holidays** Python libraries.

* The **datetime** library is introduced in the *Manipulating Dates* notebook of Chapter Two, and is further described in the introductory volume, **Background Material: An Introduction to Python for Financial Python**.  
  * A quick reference is available in: "[A Quick Introduction to Manipulating Dates](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html)".  
  * The complete introductory volume is located at: "[Background Material: An Introduction to Python for Financial Python](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/intro.html)".  
  * Consult these cited materials for a more detailed discussion of Python concepts.  
* The **holidays** library, along with the `easter` function and determining weekends, is demonstrated in the notebook, *Accounting For Non Settlement Days: Holidays, Weekends, And Good Friday*.

**Chapter Structure:**

**The chapter includes five  sections:**

1. *Actual Versus Scheduled Payment Dates* discuss the difference between scheduled and actual bond payment dates.  
2. The  Jupyter notebook *Accounting for Non-Settlement Days: Holidays, Weekends, and Good Friday* use the **holidays** and **datetime** libraries as well the dateutil.easter module to develop the adjust_bond_pay_dates function.  
3. The  Jupyter notebook *Calculating Bond Payment Dates and Amounts* converts scheduled payment dates to amounts:
   * uses the validate_date and scheduled_pay_dates functions of Chapter Two  
   * Use adjut_bond_pay_dates function of the notebook *Accounting for Non-Settlement Days: Holidays, Weekends, and Good Friday*  
   * Develops the function bond_pay_data that returns actual payment dates from a bond's maturity, coupon, annual frequency of payment, and the settlement date. 
   * an exercise asking you to calculate the payment dates and amounts for five bonds.
4. *Calculating Actual Payment Dates and Amounts*  summarizes the financial concepts and results.  
5. *Functions Imported by Accrued Interest*  describes the function imported from DropBox (*module\_basic\_concepts\_fixed\_income*).
```{tableofcontents}
```
