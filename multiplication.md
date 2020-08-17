# Multiplication

## Scenarios

### Scenario: Zero value multiplication

  Given The calculator is ON able to enter fraction
  When I type in "0"
  And I press "multiply"
  And I type in "number"
  And I press "equals"
  Then I see the "0" as the result

### Scenario: Decimal value multiplication
  
  Given The calculator is ON able to enter number
  When I type in "decimal number"
  And I press "Multiply"
  And I type in "decimal number"
  And I press "equals"
  Then I see the "Multiplied number at most 10 decimal place" as the result

### Scenario: Irrational value multiplication
  
  Given The calculator is ON able to enter decimal number
  When I type in "Irrational number"
  And I press "plus"
  And I type in "Irrational number"
  And I press "equals"
  Then I see the "Multiplied number till 10 decimal precision" as the result

### Scenario: Rational multiplication

  Given The calculator is ON able to enter operator and number
  When I type in "Rational number"
  And I press "multiply"
  And I type in "Rational number"
  And I press "equals"
  Then I see the "Multiplied number" as the result

### Scenario: Decimal & integer multiplication

  Given The calculator is ON able to enter number
  When I type in "Decimal number"
  And I press "multiply"
  And I type in "integer number"
  And I press "equals"
  Then I see the "Decimal number with sign" as the result
  
### Scenario: both numbers are positive multiplication
  
  Given The calculator is ON
  When I type in "positive number"
  And I press "Multiply"
  And I type in "positive number"
  And I press "equals"
  Then I see the "Multiplied number" as the result

### Scenario: one number negative
  
  Given The calculator is ON
  When I type in "positive number"
  And I press "Multiply"
  And I type in "negative number"
  And I press "equals"
  Then I see the "Multiplied negative number" as the result

### Scenario: both numbers negative
  
  Given The calculator is ON
  When I type in "negative number"
  And I press "Multiply"
  And I type in "negative number"
  And I press "equals"
  Then I see the "Multiplied positive number" as the result

### Scenario: Result overflow

  Given The calculator is ON able to enter big number
  When I type in "number"
  And I press "multiply"
  And I type in "number"
  And I press "equals"
  Then I see the result in 10 raise to the power

### Scenario: More than two numbers multiplication

  Given The calculator is ON able to enter number
  When I type in "number"
  And I press "multiply"
  And I type in "number"
  And I press "multiply"
  And I type in "number"
  Then I see the "left to right multiplied number" as result

### Scenario: Range of operand exceeds allowed limit

  Given The calculator is ON able to enter number
  When I type in "Operand"
  And it exceed limit
  Then I see stop taking input and wait for operator
  
### Scenario: Pressing "multiply button" more than one time

  Given: the calculator is ON
  And I type in "number"
  And I press "multiply"
  And I press "multiply"
  Don't take input until the operand, plus, minus
  And I type in "number"
  And I press "equal"
  Then I see "Multiplied number" as the result

### Scenario: Interleaving operators (Press *, then press /, then press +)

  Given: the calculator is ON
  And I type in "number"
  And I press "plus"
  And I type in "number"
  And I press "multiply"
  And I type in "number"
  And I press "equal"
  Then I see "Compute from left to right" as the result

### Scenario: Decimal value capping

  Given: the calculator is ON
  And I type in "decimal number"
  And I press "multiply"
  And I type in "number"
  And I press "equal"
  Then I see "show after decimal tell 10 digit" as the result

### Scenario: Complex number multiplication

  Given: the calculator is ON
  And I press "Ci" for Complex number computation
  And I type in "complex number"
  And I press "multiply"
  And I type in "complex number or real number"
  And I press "equal"
  Then I see "Multiplied result" as the result
