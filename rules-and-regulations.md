# 🚫 Rules and Regulations

Consult this FAQ for help regarding the rules and regulations of the competition.

## :game_die: 1. Game

Consult this section to learn about the game your AI player will be playing.

### 1.1. What game are we scripting for?

[Dots and Boxes](https://en.wikipedia.org/wiki/Dots_and_boxes). It is a simple pen and paper game you play with at minimum 2 people. The game board is a grid of dots drawn on a piece of paper.

### 1.2. How is it played?

Players take turns drawing lines between the dots. Whenever four lines are drawn around an empty box the player to draw the last line puts an initial inside of the box. Thus, they _capture_ that box and score a point.

### 1.3. When does the game end?

Play is continued until every empty box on the game board has been captured.

### 1.4. How is the winner determined?

The player who scored the most points through captures wins.

### 1.5. Do players take another turn after a capture?

Yes. Players who capture a box after drawing a line will get to immediately make another move. This also chains. So, if player scores _another_ capture after the first one they can go again, ad infinitum.

### 1.6. How is it determined who goes first?

The initial selection of who goes first in a matchup will be determined through a random number generator. After that, who ever lost the previous game in a matchup will go first.

### 1.7. What happens if I make an illegal move?

Your AI player will forfeit that specific game in a match.

## :outbox_tray: 2. Code Submission

Consult this section for help with submitting the code for your AI player.

### 2.1. How do I submit my code?

You _don't_ in a traditional sense of uploading your code to some portal. The automated tournament bracket software will automatically clone your git repository when it runs.

### 2.2. Do I need to format my code in any way?

No, there are no guidelines about formatting your code. Additionally, you will not be scored in any way regarding formatting either.

### 2.3. Do I need to document my code in any way?

No, there are no guidelines about documenting your code through comments or supplemental material. Additionally, you will not be scored in any way regarding documentation either.

### 2.4. Which files do I submit for my player?

The automated tournament bracket software will _always_ load the `mod.js` (or `mod.ts`, if using TypeScript) file as the entry point to your AI player. So, you need only the entry point and any other code files the entry point file imports.

### 2.5. How many players can I submit for the competition?

You can only submit _one_ entry point file as your submission for the competition. That being said, you can have your entry point file import any number of AI players and swap between them based on the state of the board.

## :speaking_head: 3. Consulting External Sources

Consult this section for regulations regarding the consultation of external sources outside of your brain.

### 3.1. Can I consult other people for the competition?

Yes, but under limited conditions. You are _permitted_ to talk general ideas regarding strategies and code with people outside of your team. Those people however are _not allowed_ to dictate your strategy nor are they allowed to write your code in any form.

### 3.2. Can I consult the internet (or reference material) for the competition?

Yes, but under limited conditions. You are _permitted_ to search the internet for JavaScript and TypeScript tutorials, API references, etc. You are _not allowed_ to copy code or look up game strategies.

### 3.4. Can I consult generative AI (like ChatGPT) for the competition?

Yes, but under limited conditions. You are permitted to talk general ideas regarding programming with generative AI. You are _not allowed_ to talk about strategies with generative AI nor have it write code for you.

### 3.5. Can I consult the competition organizers for the competition?

Yes, but this should be your last resort. Competition organizers, like yourself, are all students. They have _limited availability_ to help you. That being said, the touranment organizers _are permitted_ to help you with how to participate in the competition and how to use the competition software. They are _not allowed_ to talk strategies or write code with and for you.

## :crossed_swords: 4. Competition Organization

Consult this section learn about how the compeition works.

### 4.1. How is the competition ran?

Every competitor will be put in a manifest file containing their team name and git repository URL. The git repositories will automatically cloned by the tournament bracket software. Competitors' AI players will compete against each other in a standard knockout-style tournament bracket.

### 4.2. What happens if there are not enough competitors?

Touranment brackets are typically made up of powers of 2 competitors. If there are not enough competitors, then the provided sample strategic player will fill up the remaining slots. Use the sample strategic player an initial goalpost on who to beat.

### 4.3. When are the practice brackets ran?

Practice tournament brackets begin after the sign up timeframe ends. They will be automated and held every day, six times a day. The bracket ordering change between days. So as you make changes through out the day, check back to see if your AI player is doing better in the same bracket that day.

### 4.4. When will the final tournament bracket results be announced?

The club meeting following the end of the practice tournament bracket timeframe.

### 4.5. How many matches are there in a given matchup?

Bracket matchups are based on the best-of-five matches. First player to three wins takes the matchup.

### 4.6. What happens if my player throws an error during a matchup?

Your AI player will forfeit the that specific match.

### 4.7. What happens if a match ends up a draw?

If a match ends up in a draw, then the matchup will continue onto the next of five matches.

### 4.8. Is there sudden death if matchup ends up as a stalemate?

Yes, there will be three additional sudden death matches performed. The first player to win one of these matches takes the matchup.

### 4.9. What happens if there is still a draw after sudden death?

If no AI player scores wins three matches between the best-of-five matches and the sudden death matches, then a winner will be chosen at random.

### 4.10. Will I be able to see the results individual matches of a matchup?

Due to time constraints, the competition software's tournament bracket landing page will not report individual match results.

However, the raw JSON logs will be available for download upon request. Please contact a competition organizer for more information.

### 4.11. Does the dimensions of the game board change at all?

Yes, the final round will be played on a _7 columns x 5 rows_ game board. The semi-final round will be on a _6x4_ game board. And every other round before those will be on a _5x3_ game board. Make sure your AI player's strategy is _flexible_ for the additional complexity of the bigger game boards.

### 4.12. How are the winners of the competition determined?

For first place, the winner is simply the competitor who won the final round of the bracket. Then, second place is the competitor who lost to the first place player in the semi-final round.

The third-place player is determined by having the competitors who lost to the first and second place competitors in the round before the semi-final round compete in an additional bracket.

### 4.13. Are there prizes for the determined winners?

Yes, prizes will be based on first, second, and third place placements. The prizes themselves will be announced at a later date.
