# Division

## Scenarios

## Scenario:Division by Zero

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
  and enter zero,
   and press "equals".
- Then: Display "Can not divide by zero" as the result.

## Scenario: Divide 0 by any number

- Given: On the calculator
- When: Enter zero,
  and then enter "division" operator,
  and enter second "number",
   and press "equals".
- Then: Display Zero as the result.

## Scenario: One number is negative

- Given: On the calculator
- When: Enter first "positive number",
  and then enter "division" operator,
  and enter second "negative point",
   and press "equals".
- Then: Display "Divided number" with negative sign as the result.

## Scenario: Both number are negative

- Given: On the calculator
- When: Enter first "negative number",
  and then enter "division" operator,
  and enter second "negative point",
   and press "equals".
- Then: Display "Divided number" with positive sign as the result.

## Scenario: Both number are zero

- Given: On the calculator
- When: Enter zero,
  and then enter "division" operator,
  and enter zero,
   and press "equals".
- Then: Display "undefined" as the result.

## Scenario: Recurring decimal case

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
  and enter second "number",
   and press "equals".
- Then: Display "divided number" with n precision as the result.

## Scenario: Pressing division operator more than one

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
  and then enter "division" operator,
  and enter second "number",
   and press "equals".
- Then: Use one division operator and display "divided number" as the result.

## Scenario: Interleaving operators

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
  and then some irrelevant operator.
  and enter second "number",
   and press "equals".
- Then: Prefer the last operator.
       Display result accordingly.

## Scenario: Operand two is not present

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
   and press "equals".
- Then: Maintain the last state and waits for the second operand.

## Scenario: division with more than two numbers

- Given: On the calculator
- When: Enter first "number",
  and enter "division" operator,
  and then enter second "number",
   and press "equals".
- Then: Display "divided number" as the intermediate result.
- When: Again press "division" operator,
         then enter third "number",
         then press "equal".
- Then: Use intermediate result as first number and add third
        number with this as second number and
        display the final "divided number" as result.

## Scenario: Division by any/all operands being fractions

- Given: On the calculator
- When: Enter first "umber",
  and then enter "division" operator,
  and enter second "factional number",
   and press "equals".
- Then: Perform the same operation as last case.
        division with more than two numbers.

## Scenario: Simple division

- Given: On the calculator
- When: Enter first "number",
  and then enter "division" operator,
  and enter second "number",
   and press "equals".
- Then: Display "Divided number" as the result.
