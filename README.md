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

| Branch          | Purpose                         | Changes                                                                                          |
|-----------------|---------------------------------|--------------------------------------------------------------------------------------------------|
| `main`          | Stable production branch        | ---                                                                                              |
| `dev`           | Integration branch for features |                                                                                                  |
| `feature1`      | Quit/Replay feature             | Quit with a negative number, play again with 0                                                   |
| `feature2`      | Attempt Limit                   | Max_Attempts = 10, game-over state when attempts run out, shows remaining                        |
| `feature3`      | Hint System                     | after 3 attempts within 10 "You're very close!" and within 20 with 5+ attempts "Getting warmer!" |
| `hotfix`        | Production bug fix | ???                                                                                              |???                                                                                             |
| `documentation` | Project documentation           | This README                                                                                      |

##Notes
Accidentally commited this README to 'dev' instead of 'documentation' branch. 
Fixed it by cherry-picking the commit onto 'documentation' and resetting 'dev' back to the commit before it using reset --hard

##Learning Summary

Merge combines two branches as they are. If they diverge then it creates a merge commit like with feature1
to see where the code cam from. 
Rebase takes your branch's commits and replays them on by one on another branch and they get ne hashes. 45aa640 is now f4e7de4 and the history stays
without a merge commit. It's cleaner but you lose that history where the code came from.
Cherry-picking copies a commit and applies it to another branch. It creates a new commit with a new hash. It's useful for bug fixes and documentation updates.
The reason we moved it over was so that dev has the fix as well.
The trickiest part was rebasing and seeing what pieces I needed to combine, keep and straight up remove. Sure, the green parts were easy but it got really tricky in the middle with the guessing logic.
