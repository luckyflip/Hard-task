### Task


Bank "Capital Capitals" was required to write a calculator for calculating the mortgage payments, and they decided to entrust this task to you.

Write a function that will take the interest rate, down payment amount, loan amount and term (loan expiration date) as arguments and return the amount that the client will eventually pay (down payment, principal repayment, interest on the loan).

Do not forget that you must work with numbers: if the function parameter is a string, then try converting to a number. In all other cases, return the string:  `Parameter <parameter name> contains an invalid value <parameter value>` .

Please note that in the input the user specifies the end date, so in the function it is necessary to calculate the period in months based on the entered date. (you will need to use the built-in Date object)

### Implementation process:
1. activate "use strict".
2. Check the correctness of the entered data.
3. Calculate the body of the loan: the amount to be returned to the bank (the loan amount minus the down payment).
4. Calculate for how long the loan was issued (in months).
5. The monthly payment is calculated using the formula: `Payment = S * (P + P / (((1 + P) ^ n) - 1))`, where:
`S` - the body of the loan,` P` - 1/12 of the interest rate (from 0 to 1), `n` - the number of months
`^` - exponentiation
6. Calculate the total amount that the client will have to pay.
7. Round the result to two decimal places.
8. Print the result to the console and also return it from the function. The result of the function must be a numeric value.

Examples of results:

Input: interest * 100, initial payment, loan amount, term in months

Input: 10, 0, 50000, 12. Output: 52749.53

Input: 10, 1000, 50000, 12. Output: 51694.54

Input: 10, 0, 20000, 24. Output: 22149.56

Input: 10, 1000, 20000, 24. Output: 21042.09

Input: 10, 20,000, 20,000, 24. Output: 0

Input: 10, 0, 10000, 36. Output: 11616.19

Input: 15, 0, 10000, 36. Output: 12479.52

**IMPORTANT**
In clause 5 `P` - the interest rate must be a fractional number, therefore, the input data must be divided by 100.