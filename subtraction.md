# Subtraction

## Scenarios

### Scenario: Subtraction of decimals
  
  Given The calculator is ON able to enter decimal number
  When I enter in "positive decimal number"
  And I enter "minus"
  And I enter in "positive decimal number"
  And I enter "equals"
  Then I see the "subtracted decimal number" as the result

### Scenario: Typing operator more than once

  Given The calculator is ON able to enter operator and number
  When I enter in "number"
  And I enter "minus"
  And I enter "minus"
  And I enter in "number"
  And I enter "equals"
  Then I see the "subtracted number" as the result as it will prefer the first operator

### Scenario: Subtraction of more than two numbers

  Given The calculator is ON able to enter number
  When I enter in "number"
  And I enter "minus"
  And I enter in "number"
  And I enter "minus"
  And I enter in "number"
  And I enter "equals"
  Then I see the "subtracted number" as the result from left to right

### Scenario: Subtracting numbers where the result goes out of range

  Given The calculator is ON able to enter big number
  When I enter in "number"
  And I enter "minus"
  And I enter in "number"
  And I enter "equals"
  Then I see the result within the range

### Scenario: 6-* provided as input

  Given The calculator is ON able to enter number
  When I enter in "number"
  And I enter "minus"
  And I enter "multiply"
  And I enter "plus"
  Then I will wait for next operand if the immediate operator is not plus or minus
  if the immediate  operator is puls or minus
  And I will check Immediate previous operator is minus
  Then i will wait for operand
  
### Scenario: Subtraction of two positive numbers

  Given The calculator is ON
  When I enter in "positive number"
  And I enter "minus"
  And I enter in "positive number"
  And I enter "equals"
  Then I see the "subtracted number" as the result

### Scenario: Subtraction of two negative numbers
  
  Given The calculator is ON
  When I enter in "negative number"
  And I enter "minus"
  And I enter in "negative number"
  And I enter "equals"
  Then I see the "subtracted number" as the result

### Scenario: Subtraction of fractions

  Given The calculator is ON able to enter fraction
  When I enter in "number"
  And I enter "minus"
  And I enter in "number"
  And I enter "equals"
  Then I see the "subtracted number" as the result

### Scenario: Subtraction of positive and negative number
  
  Given The calculator is ON able to enter number
  When I enter in "positive number"
  And I enter "minus"
  And I enter in "negative number"
  And I enter "equals"
  Then I see the "subtracted number" as the result

### Scenario: Identify operation

  Given The calculator is ON able to enter number
  When I enter in "Identity"
  And I enter "minus"
  And I enter in "number"
  And I enter "equals"
  Then I see the "subtracted number" as the result
  
### Scenario: Converse operation

  Given: the calculator is ON
  And I enter in "operand two"
  And I enter "minus"
  And I enter in "operand one"
  Then I see the "subtracted number" as the result
