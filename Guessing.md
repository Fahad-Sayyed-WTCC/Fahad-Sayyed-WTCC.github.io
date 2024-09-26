# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateRandom[Generate random number]
    GenerateRandom --> Input[Prompt user for a guess]
    Input --> Validate[Validate user input]
    
    Validate -->|Non-numeric input| Error[Display error: Please enter a number]
    Error --> Input
    
    Validate -->|Valid input| Compare[Compare guess with random number]
    
    Compare -->|Guess is too low| TooLow[Display: Guess is too low]
    TooLow --> Input
    
    Compare -->|Guess is too high| TooHigh[Display: Guess is too high]
    TooHigh --> Input
    
    Compare -->|Correct guess| Correct[Display: Correct! You win!]
    Correct --> End([End])
