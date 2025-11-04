# Accrued Interest

**Chapter Two of the Volume *Basic Concepts of Fixed Income***.

**Highlights of the Chapter are:**

* ***Financial Concepts***

    * *Quoted verss transaction prices pf bpmds*
    * *The clean price of a bond*
    * *The dirty price of a bond*
    * *Accrued interest*

* ***Python Concepts***

    * *NumPy arrays*
    * *Python DataFrames*
    * *Accesing data with a URL address*
    * *Custom modules*
    * *The Pandas apply method*
    * *Saving DataFrames as spreadsheets*

## Background


<div style="font-family: 'Garamond', serif;
    font-size: 16px;
    text-indent: 0.25in;
    line-height: 1.5;">

This chapter uses the Python libraries Pandas and NumPy. The basic usage of these libraries is detailed in three Notebooks: "[A Quick Introduction to Pandas](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_Pandas.html)" reviews some basic concepts of Pandas, "[A Quick Introduction to NumPy](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html)" and "[A Quick Introduction to Manipulating Dates](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html)"  do the same for NumPy and the datetime module. These Notebooks are part of the introductory volume [Background Material: An Introduction to Python for Financial Python](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/intro.html). Portions of the volume will be cited throughout this chapter. Feel free to consult these materials as needed for greater discussion of Python concepts.
</div>
</br>

## Chapter Two: A Road Map

<span style="font-family: 'Garamond', serif;
    font-size: 16px;
    text-indent: 0.25in;
    line-height: 1.5;">

**1. Quoted and transaction prices of bonds**

**2. Accrued interest for Government bonds**


 **5. Accrued intrerest for non-governmnet bonds**


 **4. Calculatng accrued interest for 304 Government bonds**


 **Chapter Exercise: Calculate and save an Excel workbook with accrued interest**
</span>


**The Chapter includes Four sections.**


1. *Introduction To The Mechanics Of Bond Pricing*.  
2. The Jupyter notebook *Dealing With Dates*.
2. The  Jupyter notebook *Accrued Interest* that:  
3. *Summary* summarizes the financial concepts and results.  
4. *Functions Imported By Accrued Interest* describes the functions imported from DropBox. (*module\_basic\_concepts\_fixed\_income*)..

**Interacting with Jupyter Notebooks**

The Jupyter notebooks can be viewed just as you are viewing this page; however, they offer deeper interactive capabilities.  For example the upper-right corner of *Accrued Interest* shows icons for launching and downloading the notebook.  Downloading needs no elaboration.  The launch icon offers three options:

* **Binder:**
    * Launches in a new browser tab, typically within a minute. 
    * Supports up to one hundred simultaneous users.
    * Functions like any other Jupyter notebook, but runs remotely.
    * Allows you to:
        * Execute existing cells.
        * Add or modify cells.
        * Download the notebook.
    * Note: In this mode the notebook will not be available if saved. 

* **Colab:**
    * Offers the quickest and easiest access without requiring Binder.
        * A Google Drive is not necessary for launching.
        * You can download the notebook without signing into a Google account.
    * Note: You must sign in to a Google account to execute cells or make a copy.
      

* **Live Code:**
    * Requires a Binder launch and is ideal for demonstrations.
    * Enables you to:
        * Run code in existing cells.
        * Alter code in existing cells.
    * Note: You cannot add cells or save results in this mode.

**Any code cell in a notebook or code block in a text cell can be copied to the clipboard by moving your cursor to upper-right corner of the code cell or code block.**


```{tableofcontents}
```
