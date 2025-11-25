# Actual Versus Scheduled Payment Dates

A bond's accrued interest is calculated based on scheduled payment amounts and dates, but its present value relies on the actual amounts and dates. Although the payment amounts are fixed, the actual payment dates often deviate from the scheduled ones.

Actual payment dates correspond to settlement dates, while scheduled payments are determined relative to the bond's maturity date. Since settlement days exclude weekends, holidays, and Good Friday, any payments scheduled for these days are advanced to the next available settlement day.

The notebook *Non Settlement Days* introduces the <font color='green'>adust_bond_pay_dates()</font> function. This function takes a date object and returns a settlement date, utilizing the **holidays** library, the `easter` function from the **datetutil** module, and the <font color='green'>validate_date()</font> function developed in the *Calculating Accrued Interest* notebook.

Subsequently, the *Calculating Bond Payment Dates and Amounts* notebook utilizes <font color='green'>adust_bond_pay_dates</font> to convert scheduled payment dates into actual payment dates. The scheduled dates themselves are generated using the <font color='green'>scheduled_pay_dates</font> helper function, developed in Chapter Two's *Calculating Accrued Interest* notebook. The function, <font color='green'>bond_pay_data</font>, returns two NumPy arrays: one for the payment dates and one for the corresponding payment amounts.

Both the <font color='green'>bond_pay_data</font> and <font color='green'>accrued_interest</font> functions are essential for financial calculations presented in the later chapters of the *Basic Concepts Of Fixed Income* volume.
