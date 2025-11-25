# Getting Bomd Transaction Prices and Actual Payment Dates and Amounts

Chapters Two and Three introduce skills that allow us to expand our knowledge of the term structure of interest rates. These chapters develop two key functions that are included in the custom module *module\_basic\_concepts\_fixed\_income.py* module (referred to as *basic\_concepts\_fixed\_income*), that is available from Dropbox:

* ***accrued\_interest()***: This function is essential for converting a bond's quoted price into its actual transaction price.  
* ***bond\_pay\_data()***: This function calculates the exact dates and amounts of a bond's payments, information critical for determining the present value factors, or zero prices, required for bond pricing.

These two functions will be imported and used in later chapters. For instance, the next chapter, *Bootstrapping The Term Structure*, utilizes both the *accrued\_interest()* and *bond\_pay\_data()* functions to compute the term structure based on 304 coupon bonds. Chapter One determined the term structure for a few specific dates, Chapter Four expands on this by calculating it for 149 dates.
