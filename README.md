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
