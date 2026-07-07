# Route Optimization Visualizer

A Streamlit project brief for an interactive route optimization workbench. The app is designed to let users create or load weighted graphs, choose pathfinding algorithms, and visualize how routes are discovered between two nodes.

Project Brief: [Route Optimization Visualizer PDF](outputs/Route%20Optimization%20Visualizer.pdf)

## Project Files

```text
route-optimization-visualizer/
|-- outputs/
|   `-- Route Optimization Visualizer.pdf
`-- README.md
```

## Goal

Build a polished portfolio-ready web app that visualizes graph traversal and shortest-path algorithms with clean controls, useful metrics, and smooth animation.

The intended app should support generated graphs, manually created graphs, and uploaded CSV graph data.

## Tech Stack

- Python 3.12+
- Streamlit
- NetworkX
- Plotly or Matplotlib
- NumPy
- pandas, if needed for CSV input

## Planned Features

- Generate random weighted graphs with configurable node count, edge probability, and weight range.
- Create custom graphs manually.
- Upload graph data from CSV files.
- Toggle directed or undirected graph behavior.
- Toggle weighted or unweighted graph behavior.
- Select a start node and goal node.
- Animate algorithm progress with play, pause, next step, previous step, reset, and speed controls.
- Highlight the current node, explored nodes, frontier, edge weights, and final path.
- Show metrics after execution, including total distance, visited nodes, runtime, explored edges, path length, and memory estimate.
- Compare multiple algorithms on the same graph with a table and charts.

## Algorithms

The project brief calls for pathfinding algorithms to be implemented from scratch instead of relying on built-in shortest-path helpers.

- Breadth-First Search for unweighted graphs.
- Depth-First Search with traversal order and stack behavior.
- Dijkstra using a priority queue, distance table, visited nodes, and predecessor tracking.
- A* using x/y node coordinates and Euclidean distance as the heuristic.

## CSV Graph Format

Uploaded graph files should use this structure:

```csv
source,target,weight
A,B,4
A,C,2
C,D,5
```

## Target App Structure

The full implementation is expected to use a modular layout similar to:

```text
route-optimization-visualizer/
|-- app.py
|-- requirements.txt
|-- README.md
|-- algorithms/
|   |-- bfs.py
|   |-- dfs.py
|   |-- dijkstra.py
|   |-- astar.py
|   `-- helpers.py
|-- graph/
|   |-- graph_generator.py
|   |-- graph_loader.py
|   `-- visualization.py
|-- utils/
|   |-- metrics.py
|   `-- session.py
|-- assets/
|   `-- screenshots/
`-- data/
```

## Run Target

Once the Streamlit implementation files are added, the app should run with:

```powershell
streamlit run app.py
```

The project brief also calls for deployment support on Streamlit Community Cloud.

## Notes

This repository currently contains the exported PDF project brief. The README is written as a GitHub-rendered project overview so the repository homepage describes the intended application without requiring visitors to open the PDF first.
