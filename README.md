# Number Guessing Game

A console-based number guessing game written in Java and built with Gradle.

## Running the project

- Run the game: `gradle run --console=plain -q`
- Run the tests: `gradle test`

## Project structure

- `src/main/java/` - game source code
  - `Main.java` - entry point; creates the engine and UI
  - `GameEngine.java` - game logic (target number, guesses, attempts)
  - `GameUI.java` - console input/output loop
  - `GuessResult.java` - result of a single guess
  - `Utils.java` - random number generation and input parsing
- `src/test/java/` - JUnit tests

## Branch structure (at the start of the project)

| Branch | Purpose                         | Changes                                        |
|---|---------------------------------|------------------------------------------------|
| `main` | Stable production branch        | ???                                            |
| `dev` | Integration branch for features | Quit with a negative number, play again with 0 |
| `feature1` | Quit/Replay feature             | ???                                            |
| `feature2` | Attempt Limit                   | ???                                            |
| `feature3` | Hint System                     | ???                                            |
| `hotfix` | ???                             | ???                                            |
| `documentation` | Project documentation           | This README                                    |
