# Addition

Scenario: Addition of two positive number
  
Given that I turn on the calculator
When I type in "positive number" And I press "plus" And I type in "positive number" And I press "equals"
Then I see the "added number" as the result

Scenario: Addition of two negative number
Given that I turn on the calculator
When I type in "negative number" And I press "plus" And I type in "negative number" And I press "equals"
Then I see the "added number" as the result

Scenario: Addition of two fraction number
Given that I turn on the calculator
When I type in "fraction number" And I press "plus" And I type in "fraction number" And I press "equals"
Then I see the "added number in fraction" as the result

Scenario: Addition of two decimal number
Given that I turn on the calculator
When I type in "decimal number" And I press "plus" And I type in "decimal number" And I press "equals"
Then I see the "added number with precision up to 2 digits" as the result

Scenario: Addition of positive and negative number
Given that I turn on the calculator
When I type in "positive number" And I press "plus" And I type in "negative number" And I press "equals"
Then I see the "added number" as the result

Scenario: Typing operators more than once
Given that I turn on the calculator
When I type in "positive/negative number" And I press "plus twice" And I type in "positive/negative number" And I press "equals"
Then I see the error message as invalid operation


