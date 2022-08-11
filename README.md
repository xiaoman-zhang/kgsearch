# KGSearch

KGSearch is a minimalist tool for searching and viewing entities in a graph and is dedicated to a local environment. The application provides a Python client with three distinct terminal commands: `add, start, open`. The application default proposes to search the knowledge graph [Countries](https://www.aaai.org/ocs/index.php/SSS/SSS15/paper/view/10257/10026). You can explore the borders we must cross to get from one country to another and see how small the world is.

![](kgsearch.gif)

```sh
pip install git+https://github.com/raphaelsty/kgsearch
```

## Quick Start

The `start` command starts the API and opens the user interface:


```sh
kg start
```

## Custom KG

We can add our graph to KGSearch via the command:

```sh
kg add -f data.csv
```

The graph must be saved in CSV format and structured as triples (head, relation, tail) with a comma separator and without column names. Here is an example of a compatible CSV file:

```sh
senegal,neighbor,gambia
senegal,neighbor,mauritania
senegal,neighbor,mali
senegal,neighbor,guinea-bissau
senegal,neighbor,guinea
```

## Notes

If you have already started the application, you can reopen a window with the open command:

```sh
kg open
```

The library [Cherche](https://github.com/raphaelsty/cherche) provides the entity search engine. KGSearch relies on a local flask API. The user interface is developed in React and uses the [3D Force-Directed Graph] library (https://github.com/vasturiano/3d-force-graph).