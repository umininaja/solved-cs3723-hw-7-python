Download Link: https://assignmentchef.com/product/solved-cs3723-hw-7-python
<br>



<strong> </strong>

Write two Python programs. One that converts a number to a Roman Numeral (roman.py), and the other converts it back to a number(namor.py). Each one should accept one or more values using sys.argv(1:).




For both programs, you MUST use a function to do the conversion.  For roman.py, define a function that takes a number and returns the string. For namor.py, the function takes a string and returns a number.




You MUST submit code and some sample output for each (submit 2 .py files and 2 output files). Some comments should be present in your code (no fixed rules) and a little bit of discussion is encouraged.







<ol>

 <li>Given a number, return a Roman Numeral string. (10 points)</li>

 <li>Any number &lt;= 0 or &gt; 3,999, or invalid number, return “Error”.</li>

 <li>Use <em>only</em> these standard values (<a href="https://en.wikipedia.org/wiki/Roman_numerals">wikipedia.org/wiki/Roman_numerals</a>).</li>

 <li>Assume the input is a number and not a string.</li>

</ol>







1 = I

2 = II

3 = III

4 = IV

5 = V

6 = VI

7 = VII

8 = VIII

9 = IX10 = X

20 = XX

30 = XXX

40 = XL

50 = L

60 = LX

70 = LXX

80 = LXXX

90 = XC

100 = C

200 = CC

300 = CCC

400 = CD

500 = D

600 = DC

700 = DCC

800 = DCCC

900 = CM1000 = M

2000 = MM

3000 = MMM







Examples:

74 = LXXIV

299 = CCXCIX

2019 = MMXIX




Examples:

roman.py 812 43 prints “812 is DCCCXII” and “43 is XLIII”

roman.py 49 5000 prints “49 is XLIX” and “5000 is Error”




Hints for Part I:

<ol>

 <li>Look at thousands then hundreds then tens then ones.</li>

 <li>Create 4 Lists and put “” for the zero values.</li>

</ol>

E.g., tens = [“”, “X”, “XX”, “XXX”, “XL”, “L”, …, “XC”]

<ol start="3">

 <li>Use // for integer divide and % for remainder.</li>

</ol>







<ol>

 <li>Given a Roman Numeral String, parse it and return the number. If it does not match a legal number from above (in the range 1 to 3,999), return -1. (20 points)</li>

</ol>




Examples:

namor.py CCCXIV prints “CCCXIV is 314”

namor.py MCMXCIX prints “MCMXCIX is 1999”

namor.py CXXXXI prints “CXXXXI is -1”

namor.py 123 MMMM II prints “123 is -1” and “MMMM is -1” and “II is 2”




Hints for Part II:

<ol>

 <li>Use 4 dictionaries instead of Lists. Use dict.items() method.</li>

</ol>

E.g., tens = {“XC”: 90, “LXXX”: 80, “LXX”: 70, …, “X”: 10}

<ol start="2">

 <li>Very Important: Put each dictionary in reverse order</li>

</ol>

E.g., look for XC then LXXX then LXX then LX then L, etc.

<ol start="3">

 <li>Use the str.upper() and str.startswith() methods.</li>

</ol>








