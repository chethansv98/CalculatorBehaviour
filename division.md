# Division

## Scenarios

### Scenario: Recurring decimal case

  Given The calculator is ON able to enter operator and number
  When I type in "number"
  And I press "divide"
  And I type in "number"
  And I press "equals"
  Then I see the "at most ten precision" as the result

### Scenario: n number of times "/" pressed

  Given The calculator is ON able to enter number
  When I type in "number"
  And I press "divide"
  And I Press "divide"
  And I type in "number"
  And I press "equals"
  Then I see "divided number" as the result if immediate operator is not plus / minus
  if the immediate  operator is puls or minus
  And I will check Immediate previous operator is minus
  Then i will wait for operand

### Scenario: When operand 2 is not present

  Given The calculator is ON able to enter big number
  When I type in "number"
  And I press "divide"
  And I press "equals"
  Then I don't see the result wait for operand

### Scenario: Division by any/all operands being fractions

  Given The calculator is ON able to enter number
  When I type in "number"
  And I press "divide"
  And I type in "fraction number"
  Then I see "Left to right division" as result

### Scenario: Division of more than 2 numbers

  Given The calculator is ON able to enter number
  When I type in "number"
  And I press "divide"
  And I type in "number"
  And I press "divide"
  And I type in "number"
  And I press "equals"
  Then I see the "left to right division" as the result

### Scenario: Division by zero when operand one is any number

Given The calculator is ON
When I type in "number"
And I press "divide"
And I type in "zero"
And I press "equals"
Then I see the "cannot divide number by zero" as the result

### Scenario: Divide zero by any number
  
  Given The calculator is ON
  When I type in "zero"
  And I press "divide"
  And I type in "number"
  And I press "equals"
  Then I see "zero" as the result

### Scenario: Any one operand is negative

  Given The calculator is ON able to enter fraction
  When I type in "operand one" positive
  And I press "divide"
  And I type in "operand two" negative
  And I press "equals"
  Then I see the "negative number" as the result

### Scenario: Both the operand is negative

  Given The calculator is ON able to enter fraction
  When I type in "operand one" negative
  And I press "divide"
  And I type in "operand two" negative
  And I press "equals"
  Then I see the "negative number" as the result

### Scenario: Division isn't symmetric
  
  Given The calculator is ON able to enter number
  When I type in "number"
  And I press "divide"
  And I type in "number"
  And I press "equals"
  Then I see the "number" as the result

### Scenario: Division when both operands are 0
  
  Given The calculator is ON able to enter decimal number
  When I type in "zero"
  And I press "divide"
  And I type in "zero"
  And I press "equals"
  Then I see the "undefined" as the result
