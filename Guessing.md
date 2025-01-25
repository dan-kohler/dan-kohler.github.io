# Guessing Game
#### Explanation:
1. **Start**: _The program begins by generating a random number within the specified range._
2. **User Input**: _Prompts the user to input their guess._
3. **Input Validation**:
   - _Checks if the input is a valid number._
   - _Ensures the guess is within the specified range._
4. **Feedback**:
   - _If the guess is too high, the program tells the user._
   - _If the guess is too low, the program provides feedback._
   - _If the guess is correct, the program congratulates the user and ends._
5. **Repeat**: _The process continues until the user guesses the correct number._

```mermaid
flowchart TD
    Start([Start]) --> B[Generate a random number within range]
    B --> C[Prompt user to guess a number]
    C --> D[Validate input: Is it a number?]
    D -- Yes --> E[Is the guess within range?]
    D -- No --> F[Show error: Invalid input, enter a number.]
    F --> C
    E -- No --> G[Show error: Guess out of range.]
    G --> C
    E -- Yes --> H[Compare guess to the random number]
    H -- Guess is too high --> I[Show message: Too high! Try again]
    H -- Guess is too low --> J[Show message: Too low! Try again]
    H -- Guess is correct --> K[Show message: Correctamundo! You win!]
    I --> C
    J --> C
    K --> L([End])
