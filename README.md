# Retex

**Boilerplate/PoC of the Rete Algorithm implementated in Elixir**

Rete is a complex stateful algorithm, this is an attempt of reproducing it with a functional immutable language
such as Elixir/Erlang. This is a boilerplate that will let you implement your own version of Rete starting from a baseline.

Feel free to contact me via email if you have any question. 

## Concepts

- Retex compiles the rules using `libgraph` (A graph data structure library for Elixir projects)
- The activation of nodes is done using a `Map.reduce` over each node and activating them
using the `Activation` protocol. Each type of node implements its own protocol for the activation
- When a node is activated, a map is updated adding its ID to the list of activated nodes in the Retex state
- A list of bindinds is passed along each iteration of the reduction on the graph and updated/checked depending on each implementation of the Activation protocol that the current node has


## TODO

- Each production node should be visited only once
- Add tests for variables of the same name in different rules (it should work, right now it isnt)
- Improve performances and extend the facts to handle more complex cases such as relationships between WMEs


## Warnings

- So far it works very little and only in some cases, needs more testing and a better way to handle variable bindings
- This is just a WIP and a PoC, do not use it in production but feel free to contribute with ideas and PRs
- Use it as boilerplate and starting point to continue your own personal implementation (more facts, DSL, etc)

## For more on Rete algorithm
- https://cis.temple.edu/~giorgio/cis587/readings/rete.html
