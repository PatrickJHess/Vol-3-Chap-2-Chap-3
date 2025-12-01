## Calculating Actual Payment Dates and Amounts

This chapter focused on the process of converting scheduled payment dates into actual payment dates. Key to this conversion was the import of the **holidays** library, as well as the <font color='green'>easter</font> function from the **dateutil** module.



**The conversion logic is encapsulated in two main functions:**

* The <font color='green'>adjusting_bond_pay_dates</font> function, which converts all scheduled non-settlement dates to actual payment dates.  
* The <font color='green'>bond_pay_data</font> function, then generates NumPy arrays for both the actual payment dates and their corresponding amounts.

**Key Takeaways**

* Converting scheduled payment dates to actual settlement dates.  
* Calculating the payment amounts associated with the actual payment dates.
