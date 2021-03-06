# PrisonersDilemmaSWHS
#### Coded by [Arthur Goldman](https://github.com/gefjon) (Minneapolis Southwest High School, Class of 2017)
Contributors:
* [Henning Tonko](https://github.com/HenningTonko) Added -r (random) argument (SWHS Class of 2018)
* [Themistocles Megas](https://github.com/Themis3000) Improved code optimization, python 3.8 support, and rule compliance. (SWHS Class of 2021)

#### Brought to you by Gabriel A Pass (PLTW Computer Science Instructor)

#### For more information contact: gabriel@gapmedia.org

This is a Python 3 implementation of the Age old problem of logic, game theory.  It was inspired by a Python 2 approach by PLTW (Project Lead the Way) for their Computer Science Principles course.  This implementation of the dilemma was coded from scratch by the Southwest High School students credited above.  Our approach provides a new formulation of the classic logic problem, with new rules, and all new opportunities to cheat ( ͡° ͜ʖ ͡°).  We are providing this Python 3 Iterated Prisoner's Dilemma to the community of Python students and developers for your enjoyment and challenge.

## Requirements

This iterated prisoner's dilemma requires `Python 3.6 or above` and depends on `pandas`.  
Pandas can be installed with:
```
python -m pip install pandas
```

With these Requirements, you are ready to run your tournament.  See the OFFICIAL_RULES for more information the competition.

Note: Python 3.6 is available for Enthought Canopy 2.1 and will come standard in Canopy 2.2
At this time, other IDEs may be easier to use.

## Running the Program

To run a tournament, Run `iterated-dilemma.py` with the names of your modules.
For example, if you have team modules named:
```
player1.py
WinningTeam.py
C:\Users\Me\Desktop\weSuck.py
```
run `./iterated-dilemma.py player1.py WinningTeam.py C:\Users\Me\Desktop\weSuck.py`. Any number of modules can be given.

Alternately, if you've got a directory that contains your modules, and the only `.py` files in it are your modules, you can use the command-line flag `-d <directory-path>`:

```
./iterated-dilemma.py -d examplemodules
```

Additional Options:
`-r` argument results in randomized player order

## Hosting a Tournament
The Iterative Prisoners Dilemma is designed to be staged on GitHub.  To host your own tournament, clone this repository and upload it as a new repository to your own GitHub account.  Each competing team can clone the repository, branch it, program and test their module solution, and send a pull request to your master branch.  Merge all your competitors branches and run the competition.  

(A Git server is not a requirement to host a tournament, however it is an ideal collaborative method to host a tournament and strongly recommended.)

* In the OFFICIAL_RULES, players are instructed to place their modules in the `tournament` directory.  
* It is usually ideal to have players also compete against classic solutions from the `examplemodules` directory.
* If you plan to include any `examplemodules` copy them to the `tournament` directory before allowing your players to clone the repository.
* Run the tournament using:
```
./iterated-dilemma.py -d tournament
```

## Notes & FAQ

Note: In PyCharm and IDEs with a RUN program function, add parameters such as `-d modules` by adding a "Run Configuration" for `iterated-dilemma.py`.  In PyCharm, make the following menu selection: [Run] > [Edit Configuration]

Note: When running the program in Cmd or PowerShell, if Python files are not set to open in Python (i.e. if `.py` files open in an IDE), You may have to do something like:

```
python iterated-dilemma.py -d examplemodules
python iterated-dilemma.py player1.py WinningTeam.py C:\Users\Me\Desktop\weSuck.py
python iterated-dilemma.py
```

Each team's module should conform to Python 3.6 and must provide several things:

`team_name`: a string, no more than 16 characters long, containing no newlines or other weird blank space (must not match regex [^a-zA-Z\d\s:.,'%`])

`strategy_name`: a string, no more than 70 characters long, containing no newlines or other weird blank space (must not match regex [^a-zA-Z\d\s:.,'%`])

`strategy_description`: a string, no more then 350 characters long, containing no newlines or other weird blank space (must not match regex [^a-zA-Z\d\s:.,'%`])

`move(my_moves, their_moves, my_score, their_score)`: a function that returns either `'b'` or `'c'` for BETRAY or COLLUDE. You can also `import GLOBALS` and return `GLOBALS.BETRAY` or `GLOBALS.COLLUDE`. `my_moves` and `their_moves` are strings containing the moves that each player has taken so far in this iterated dilemma, and `my_score` and `their_score` are ints that will usually be negative containing each player's score so far in this round.



*Enjoy!*
