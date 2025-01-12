---
title: Math 381E
subtitle: Graphs and Networks
author: Atabey Kaygun
date: Monday, May 9th, 2022
incremental: true
---

# What is a graph

## A Mathematician's Definition

A graph consists of two sets:

- A set of vertices (nodes)
- A set of edges (connections)

## A Mathematician's Definition

$$ V = \{ A, B, C, D, E \}$$

$$ E = \{ (A,B), (A,C), (B,D), (C,D), (D,E) $$ 

## An Intuitive Definition

A graph consists of nodes and connections:

~~~~ {.dot }
graph {
  node[shape=circle];
  A -- { B C } -- D -- E;
}
~~~~

$$ V = \{ A, B, C, D, E \}$$

$$ E = \{ (A,B), (A,C), (B,D), (C,D), (D,E) $$ 

## Types of Graphs

- Undirected
- Directed
- Weighted

## Undirected Graphs

The edges in an undirected graph have no direction:

![](image-1.png)

## Directed Graphs

The edges in a directed graph have direction:

~~~~ {.dot }
digraph {
  node[shape=circle];
  A -> {B C} -> D -> E -> A;
  B -> A;
}
~~~~

## Weighted Graphs

The edges in a weighted graph have weights:

~~~~ {.dot }
graph {
  node[shape=circle];
  A -- B [label=1];
  A -- C [label=2];
  B -- D [label=1];
  C -- D [label=-1];
  D -- E [label=0];
}
~~~~

# Graphs and Data

## What type of data can be represented by graphs?

Any data where we can relate two data points

- Text data
- Route information for transportation data
- Internet itself
- Friendship graphs in social networks

## Text data

- Text consists of sentences and words
- Sentences are related by words
- Words are related by sentences

## Route information for transportation

Remember HW2?

<img height="500px" src="transportation.png">

## Internet itself

![An Early Map of the Whole Internet (1973)](arpanet.png)

## My Own Research Subjects

![Atabey's Map of NCG](ncg.png)

# Tools for Graph Data

## Graph Language

[GraphViz](https://graphviz.org/) is an excellent graph definition language and visualization framework.

## Graphviz Example

```
graph {
  A -- { B C } -- { D E F } -- G;
}
```

~~~~ {.dot}
graph {
  node[shape=circle];
  A -- { B C } -- { D E F } -- G;
}
~~~~


## Python and Graphs

The three main graph toolkits are

* [igraph](https://igraph.org) 
* [graph-tool](https://graph-tool.skewed.de/static/doc/index.html)
* [networkx](https://networkx.org)

DEMO

# Graph Data 

## Examples

1. Harry Potter Character Network [[Efe Karakuş]](https://github.com/efekarakus/potter-network/tree/master/data)
2. Correlation Network 
2. PhD Hiring Network
3. Marvel Character Network [[Kaggle]](https://www.kaggle.com/datasets/dannielr/marvel-superheroes) 
4. Social Media Networks [[Steve Hadden]](https://towardsdatascience.com/how-to-download-and-visualize-your-twitter-network-f009dbbf107b)

DEMO
