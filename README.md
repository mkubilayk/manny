# MANNY

This project is based on The Pac-Man projects developed by John DeNero, Dan Klein, and Pieter Abbeel at UC Berkeley.

We implement artifical intelligence of agents in Pac-Man world. Use commands below to run the client with the desired algorithm.

You should be able to play a game of Pac-Man by typing the following at the command line:

```
$ python pacman.py
```

## Search

- [x] Depth First Search

```
$ python pacman.py -l tinyMaze -p SearchAgent
$ python pacman.py -l mediumMaze -p SearchAgent
$ python pacman.py -l bigMaze -z .5 -p SearchAgent
```

- [x] Breadth First Search

```
$ python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
$ python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5
```

- [x] Uniform Cost Search

```
$ python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs
$ python pacman.py -l mediumDottedMaze -p StayEastSearchAgent
$ python pacman.py -l mediumScaryMaze -p StayWestSearchAgent
```

- [x] A* Search

```
$ python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

## Multi-Agent Search

- [x] Reflex Agent

```
$ python pacman.py -p ReflexAgent -l testClassic
$ python pacman.py --frameTime 0 -p ReflexAgent -k 1
$ python pacman.py --frameTime 0 -p ReflexAgent -k 2
```

- [x] Minimax

```
$ python pacman.py -p MinimaxAgent -l minimaxClassic -a depth=4
$ python pacman.py -p MinimaxAgent -l trappedClassic -a depth=3
```

- [x] Alpha-Beta Pruning

```
$ python pacman.py -p AlphaBetaAgent -a depth=3 -l smallClassic
$ python pacman.py -p AlphaBetaAgent -l trappedClassic -a depth=3 -q -n 10
```

- [x] Expectimax

```
$ python pacman.py -p ExpectimaxAgent -l minimaxClassic -a depth=3
$ python pacman.py -p ExpectimaxAgent -l trappedClassic -a depth=3 -q -n 10
```

## Evaluation

These are the command for obtaining evaluation results presented in the paper.

#### Open Classic Maze

```
$ python pacman.py -p ReflexAgent -l openClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l openClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l openClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l openClassic -a depth=3 -q -n 10
```

#### Small Classic Maze

```
$ python pacman.py -p ReflexAgent -l smallClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l smallClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l smallClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l smallClassic -a depth=3 -q -n 10
```

#### Medium Classic Maze

```
$ python pacman.py -p ReflexAgent -l mediumClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l mediumClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l mediumClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l mediumClassic -a depth=3 -q -n 10
```

#### Tricky Classic Maze

```
$ python pacman.py -p ReflexAgent -l trickyClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l trickyClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l trickyClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l trickyClassic -a depth=3 -q -n 10
```

#### Minimax Classic Maze

```
$ python pacman.py -p ReflexAgent -l minimaxClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l minimaxClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l minimaxClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l minimaxClassic -a depth=3 -q -n 10
```

#### Trapped Classic Maze

```
$ python pacman.py -p ReflexAgent -l trappedClassic -q -n 10
$ python pacman.py -p MinimaxAgent -l trappedClassic -a depth=3 -q -n 10
$ python pacman.py -p AlphaBetaAgent -l trappedClassic -a depth=3 -q -n 10
$ python pacman.py -p ExpectimaxAgent -l trappedClassic -a depth=3 -q -n 10
```
