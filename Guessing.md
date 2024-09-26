flowchart TD
    Start([Start]) --> Input[Ask user for a guess]
    Input --> Validate[Check if input is valid]
    
    Validate -->|Valid input| GenerateRandom[Generate random number]
    Validate -->|Non-numeric input| Error[Display: Invalid input. Please enter a number]
    Error --> Input

    GenerateRandom --> Compare[Compare guess with random number]
    
    Compare -->|Guess is correct| Correct[Display: Correct! You win!]
    Compare -->|Guess is too low| TooLow[Display: Guess is too low, try again]
    Compare -->|Guess is too high| TooHigh[Display: Guess is too high, try again]
    
    TooLow --> Input
    TooHigh --> Input
    Correct --> End([End])
