# Organizing Scientific Paper Conferences

Code for my master thesis. The tool takes a list of papers and a set of rooms, groups papers with similar topics, and puts each group in the same room.

## How it works

1. Turns each abstract into a vector with MiniLM.
2. Groups similar papers with hierarchical clustering.
3. Assigns the groups to rooms with GRASP.
4. Checks how good the final layout is.

## How to run it

Install the packages:

```
pip install numpy pandas scipy torch sentence-transformers
```

Then run:

```
cd "Full Application"
python main.py --papers my_papers.csv --rooms 700,600,550
```

`--rooms` is the number of papers each room can hold. Each run saves its results in a new `Production N` folder.

## Folders

- `Full Application` is the finished tool.
- `Experimentation & Model Choice` has the tests I ran for the thesis: comparing models, clustering and different room layout methods.
