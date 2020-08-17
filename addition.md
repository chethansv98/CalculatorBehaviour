# Addition

## Scenario: Addition of two positive number

  Given that I turn on the calculator

  When I type in "positive number"
  And I press "plus"
  And I type in "positive number"
  And I press "equals"
  
  Then I see the "added number" as the result
