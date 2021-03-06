Video Game Troubles
===================

Farmer John's cows love their video games! FJ noticed that after
playing these games that his cows produced much more milk than
usual, surely because contented cows make more milk.

The cows disagree, though, on which is the best game console. One
cow wanted to buy the Xbox 360 to play Halo 3; another wanted to
buy the Nintendo Wii to play Super Smash Brothers Brawl; a third
wanted to play Metal Gear Solid 4 on the PlayStation 3. FJ wants
to purchase the set of game consoles and games (within the constraints
of a given budget) that helps his cows produce the most milk and
thus nourish the most children.

FJ researched N (1 <= N <= 50) consoles, each with a console price
P_i (1 <= P_i <= 1000) and a number of console-specific games G_i
(1 <= G_i <= 10). A cow must, of course, own a console before she
can buy any game that is specific to that console. Each individual
game has a game price GP_j (1 <= GP_j price <= 100) and a production
value (1 <= PV_j <= 1,000,000), which indicates how much milk a cow
will produce after playing the game. Lastly, Farmer John has a
budget V (1 <= V <= 100,000) which is the maximum amount of money
he can spend. Help him maximize the sum of the production values
of the games he buys.

Consider one dataset with N=3 consoles and a V=$800 budget. The
first console costs $300 and has 2 games with cost $30 and $25 and
production values as shown:

    Game #    Cost    Production Value
      1       $30          50
      2       $25          80

The second console costs $600 and has only 1 game:

    Game #    Cost    Production Value
      1       $50          130

The third console costs $400 and has 3 games:

    Game #    Cost    Production Value
      1       $40         70
      2       $30         40
      3       $35         60

Farmer John should buy consoles 1 and 3, game 2 for console 1, and
games 1 and 3 for console 3 to maximize his expected production at
210:

                                Production Value
        Budget:     $800      
        Console 1  -$300
           Game 2   -$25              80
        Console 3  -$400
           Game 1   -$40              70
           Game 3   -$35              60
      -------------------------------------------
        Total:         0 (>= 0)      210

PROBLEM NAME: vidgame

INPUT FORMAT:

* Line 1: Two space-separated integers: N and V

* Lines 2..N+1: Line i+1 describes the price of and the games
        available for console i; it contains: P_i, G_i, and G_i pairs
        of space-separated integers GP_j, PV_j

SAMPLE INPUT:

3 800
300 2 30 50 25 80
600 1 50 130
400 3 40 70 30 40 35 60

OUTPUT FORMAT:

* Line 1: The maximum production value that Farmer John can get with
        his budget.

SAMPLE OUTPUT:

210
