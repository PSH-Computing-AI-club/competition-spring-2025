# 🚫 Rules and Regulations

Consult this FAQ for help regarding the rules and regulations of the competition.

- [🚫 Rules and Regulations](#-rules-and-regulations)
  - [:game\_die: 1. Game](#game_die-1-game)
    - [1.1. What game are we scripting for?](#11-what-game-are-we-scripting-for)
    - [1.2. How is it played?](#12-how-is-it-played)
    - [1.3. When does the game end?](#13-when-does-the-game-end)
    - [1.4. How is the winner determined?](#14-how-is-the-winner-determined)
    - [1.5. Do players take another turn after a capture?](#15-do-players-take-another-turn-after-a-capture)
    - [1.6. How is it determined who goes first?](#16-how-is-it-determined-who-goes-first)
    - [1.7. What happens if I make an illegal move?](#17-what-happens-if-i-make-an-illegal-move)
  - [:outbox\_tray: 2. Code Submission](#outbox_tray-2-code-submission)
    - [2.1. How do I submit my code?](#21-how-do-i-submit-my-code)
    - [2.2. Do I need to format my code in any way?](#22-do-i-need-to-format-my-code-in-any-way)
    - [2.3. Do I need to document my code in any way?](#23-do-i-need-to-document-my-code-in-any-way)
    - [2.4. Which files do I submit for my player?](#24-which-files-do-i-submit-for-my-player)
    - [2.5. How many players can I submit for the competition?](#25-how-many-players-can-i-submit-for-the-competition)
  - [:speaking\_head: 3. Consulting External Sources](#speaking_head-3-consulting-external-sources)
    - [3.1. Can I consult other people for the competition?](#31-can-i-consult-other-people-for-the-competition)
    - [3.2. Can I consult the internet (or reference material) for the competition?](#32-can-i-consult-the-internet-or-reference-material-for-the-competition)
    - [3.4. Can I consult generative AI (like ChatGPT) for the competition?](#34-can-i-consult-generative-ai-like-chatgpt-for-the-competition)
    - [3.5. Can I consult the competition organizers for the competition?](#35-can-i-consult-the-competition-organizers-for-the-competition)
  - [:crossed\_swords: 4. Competition Organization](#crossed_swords-4-competition-organization)
    - [4.1. How is the competition ran?](#41-how-is-the-competition-ran)
    - [4.2. What happens if there are not enough competitors for a full bracket?](#42-what-happens-if-there-are-not-enough-competitors-for-a-full-bracket)
    - [4.3. When are the practice brackets ran?](#43-when-are-the-practice-brackets-ran)
    - [4.4. When will the final tournament bracket results be announced?](#44-when-will-the-final-tournament-bracket-results-be-announced)
    - [4.5. How many matches are there in a given matchup?](#45-how-many-matches-are-there-in-a-given-matchup)
    - [4.6. What happens if my player throws an error during a matchup?](#46-what-happens-if-my-player-throws-an-error-during-a-matchup)
    - [4.7. How long can my player take to compute its move?](#47-how-long-can-my-player-take-to-compute-its-move)
    - [4.8. What happens if a match ends up a draw?](#48-what-happens-if-a-match-ends-up-a-draw)
    - [4.9. Is there sudden death if matchup ends up as a stalemate?](#49-is-there-sudden-death-if-matchup-ends-up-as-a-stalemate)
    - [4.10. What happens if there is still a draw after sudden death?](#410-what-happens-if-there-is-still-a-draw-after-sudden-death)
    - [4.11. Will I be able to see the results individual matches of a matchup?](#411-will-i-be-able-to-see-the-results-individual-matches-of-a-matchup)
    - [4.12. Does the dimensions of the game board change at all?](#412-does-the-dimensions-of-the-game-board-change-at-all)
    - [4.13. How are the winners of the competition determined?](#413-how-are-the-winners-of-the-competition-determined)
    - [4.14. Are there prizes for the determined winners?](#414-are-there-prizes-for-the-determined-winners)

## :game_die: 1. Game

Consult this section to learn about the game your AI player will be playing.

### 1.1. What game are we scripting for?

[Dots and Boxes](https://en.wikipedia.org/wiki/Dots_and_boxes). It is a simple pen and paper game you play with at minimum 2 people. The game board is a grid of dots drawn on a piece of paper.

### 1.2. How is it played?

Players take turns drawing lines between the dots. Whenever four lines are drawn around an empty box the player to draw the last line puts an initial inside the box. Thus, they _capture_ that box and score a point.

### 1.3. When does the game end?

Play is continued until every empty box on the game board has been captured.

### 1.4. How is the winner determined?

The player who scored the most points through captures wins.

### 1.5. Do players take another turn after a capture?

Yes. Players who capture a box after drawing a line will get to immediately make another move. This also chains. So, if player scores _another_ capture after the first one they can go again, ad infinitum.

### 1.6. How is it determined who goes first?

The initial selection of who goes first in a matchup will be determined through a random number generator. After that, who ever lost the previous game in a matchup will go first.

### 1.7. What happens if I make an illegal move?

Your AI player will forfeit that specific match.

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

Consult this section for regulations regarding the consultation of external sources outside your brain.

### 3.1. Can I consult other people for the competition?

Yes, but under limited conditions. You are _permitted_ to talk general ideas regarding strategies and code with people outside your team. Those people however are _not allowed_ to dictate your strategy nor are they allowed to write your code in any form.

You can talk with other contestants and get technical support in the `#competition-support` channel on the club's Discord.

### 3.2. Can I consult the internet (or reference material) for the competition?

Yes, but under limited conditions. You are _permitted_ to search the internet for JavaScript and TypeScript tutorials, API references, etc. You are _not allowed_ to copy code or look up game strategies.

### 3.4. Can I consult generative AI (like ChatGPT) for the competition?

Yes, but under limited conditions. You are permitted to talk general ideas regarding programming with generative AI. You are _not allowed_ to talk about strategies with generative AI nor have it write code for you.

### 3.5. Can I consult the competition organizers for the competition?

Yes, but this should be your last resort. Competition organizers, like yourself, are all students. They have _limited availability_ to help you. That being said, the competition organizers _are permitted_ to help you with how to participate in the competition and how to use the competition software. They are _not allowed_ to talk strategies or write code with and for you.

## :crossed_swords: 4. Competition Organization

Consult this section learn about how the competition works.

### 4.1. How is the competition ran?

Every competitor will be put in a manifest file containing their team name and git repository URL. The git repositories will automatically be cloned by the tournament bracket software. Competitors' AI players will compete against each other in a standard knockout-style tournament bracket.

### 4.2. What happens if there are not enough competitors for a full bracket?

Tournament brackets are typically made up of powers of 2 competitors. If there are not enough competitors, then the provided sample "Split Personality" AI player will fill up the remaining slots. Use the sample "Split Personality" AI player as an initial goalpost on who to beat.

- [`split_personality.js`](https://github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes-template-javascript/blob/main/split_personality_player.js)
- [`split_personality.ts`](https://github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes-template-typescript/blob/main/split_personality_player.ts)

> [!NOTE]
> The placeholder AI player might be subject to change during the practice brackets depending on average skill level of the competitors.

### 4.3. When are the practice brackets ran?

Practice tournament brackets begin after the sign-up timeframe ends. They will be automated and held every day, six times a day. The bracket ordering change between days. So as you make changes throughout the day, check back to see if your AI player is doing better in the same bracket that day.

### 4.4. When will the final tournament bracket results be announced?

The club meeting following the end of the practice tournament bracket timeframe.

### 4.5. How many matches are there in a given matchup?

Bracket matchups are based on the best-of-five matches. First player to three wins takes the matchup.

### 4.6. What happens if my player throws an error during a matchup?

Your AI player will forfeit the that specific match.

### 4.7. How long can my player take to compute its move?

Your AI player has a time budget of 1000 milliseconds (or 1 second).

> [!NOTE]
> This restriction _might_ be subject to change in the future.

### 4.8. What happens if a match ends up a draw?

If a match ends up in a draw, then the matchup will continue onto the next of five matches.

### 4.9. Is there sudden death if matchup ends up as a stalemate?

Yes, there will be three additional sudden death matches performed. The first player to win one of these matches takes the matchup.

### 4.10. What happens if there is still a draw after sudden death?

If no AI player wins three matches between the best-of-five matches and the sudden death matches, then a winner will be chosen at random.

### 4.11. Will I be able to see the results individual matches of a matchup?

Due to time constraints, the competition software's tournament bracket landing page will not report individual match results.

However, the raw JSON logs will be available for download upon request. Please contact a competition organizer for more information.

### 4.12. Does the dimensions of the game board change at all?

Yes, the final round will be played on a _7 columns x 5 rows_ game board. The semi-final round will be on a _6x4_ game board. And every other round before those will be on a _5x3_ game board. Make sure your AI player's strategy is _flexible_ for the additional complexity of the bigger game boards.

### 4.13. How are the winners of the competition determined?

For first place, the winner is simply the competitor who won the final round of the bracket. Then, second place is the competitor who lost to the first place player in the semi-final round.

The third-place player is determined by having the competitors who lost to the first and second place competitors in the round before the semi-final round compete in an additional bracket.

### 4.14. Are there prizes for the determined winners?

Yes, prizes will be based on first, second, and third place placements. The prizes themselves will be announced at a later date.
