# Portfolio
Value / Momentum / Volume Python Equity Sorting Strategy


Looking for ways to use the power of python programming for trading decisions I stumbled upon a Youtube video of IEX-Cloud's Nick McCullum strategies for quantitative investing.

 

It featured a Value Section and Momentum section where through a sorting algorithm he found the topmost attractive equities for both strategies from a universe of comosed S&P500 stocks.

 

To find undervalued stocks, he took the average percentile of a combination of comparable ratios such as  P/E, P/B, P/S, EV/EBITDA, and EV/Gross Profit for each stock. That average is then sorted from smallest to largest with the basic idea that the stocks in the top rows after the sort can be considered to have relatively more undervalued qualities than the rest of its peers in the universe that we have chosen. 

​

The same goes with the momentum strategies by taking an average percentile of the one year, six month, three month, and one month price returns to then sort from largest to smallest. Just like with the undervalued stocks, the stocks in the top rows of the momentum strategy after the sort can be considered to have relatively more upward momentum qualities than the rest. 

​

For both strategies, the user is supposed to choose how many top-row stocks to select and the code calculates the number of charges to buy for each stock assuming an equally-weighted portfolio from an initial investment amount input.

​

I decide to extend the project by:

​

1. Adding a Volume Strategy so as to assume that the momentum of the selected stocks is also backed by actual volume and not some arbitrary price jump due for a correction. Selected Metrics include average 30-day volume, average 10-day volume, previous volume, and a Put-to-call ratio. I also adjust the volume by market-cap avoiding selection bias towards large-cap stocks which tend to have higher volume due to size. 

​

2. Adding PegRatio & EV/Revenue metrics to the Value Strategy and five-day price return to Momentum Strategy.

​

3. Combining the three strategies to get a portfolio of equities that seem to have undervalued qualities with upside volume-backed momentum. Of course, selected stocks should then be analyzed individually from a fundamental perspective aided by inner management composition/culture insights, industry multiples, and general macroeconomic outlook.

​

4. Automating Process + Adding Input Options such that the user only needs to input selected metrics for the process to output an excel file containing desired stocks.  

 

Steps:

 1. ENTER Value of Portfolio

 2. ENTER Value Bottom Percentile (as whole number)

 3. ENTER Momentum Top Percentile (as whole number)

 4. ENTER Volume Top Percentile (as whole number)

 5. DO YOU WANT to include all MAKET-CAPS? If no, enter quote-separated Market Caps (options: Large, Mid, Small).

 6. DO YOU WANT to include all INDUSTRIES? If no, enter quote-separated Industries (options: 'Manufacturing', 'Transportation, Communications, Electric, Gas, And Sanitary Services', 'Retail Trade', 'Services', 'Wholesale Trade', 'Finance, Insurance, And Real Estate', 'Not Found', 'Mining', 'Public Administration', 'Agriculture, Forestry, And Fishing', 'Construction').

​

7. Run & Wait for the Excel File containing parameter-specified equities with a row that calculates the number of shares to buy assuming an equally-weighted portfolio. 
