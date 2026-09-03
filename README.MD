# Graph Centrality Analysis - DAA Mini Project

Mini-project for the Design and Analysis of Algorithms (DAA) course, ISCTE-IUL, 2025/26.

Implements a graph library and a `CentralityAnalyser` class from scratch (BFS, connected components, diameter, degree/closeness/eigenvector/betweenness centrality), applied to character co-occurrence networks from *A Song of Ice and Fire* (Game of Thrones) and the Marvel Universe, with complexity analysis, analytical validation, and empirical runtime benchmarks.

**Authors:** Gonçalo Sobral, Rafael Silva

## Contents

The notebook is organized into five sections:

1. **CentralityAnalyzer API** - `Vertex`, `Edge`, and `Graph` base classes; `CentralityAnalyser` constructor.
2. **Structural analysis** - BFS, connected components, degree distribution, diameter.
3. **Centrality metrics** - Degree, Closeness, Eigenvector, and Betweenness centrality, each with a complexity analysis, a hand-worked analytical validation on a small graph, and results on the real datasets.
4. **Empirical runtime analysis** - scalability benchmarks across all four datasets, log-log plots, and verification of the theoretical complexity ratios against measured times.
5. **Ethical questions** - external collaborations and references.

## Repository structure

```
.
├── README.md
├── requirements.txt
├── ProjetoDAA_ENG.ipynb #ENGLISH version
├── got_book1.csv
├── got_full.csv
├── marvel_small.csv
└── marvel_full.csv
```

The notebook loads the CSVs by filename (e.g. `load_graph_csv("got_book1.csv")`), so it must be run from the repository root, with the CSVs alongside it.

## Datasets

Each CSV has three columns: `Source`, `Target`, `Weight` - an edge between two characters and the number of times they co-occur. Weight is not used in the distance/centrality calculations; BFS drives all metrics.

| Dataset | Vertices | Edges |
|---|---|---|
| got_book1.csv | 187 | 684 |
| got_full.csv | 796 | 2,823 |
| marvel_small.csv | 327 | 9,891 |
| marvel_full.csv | 6,421 | 167,112 |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook ProjetoDAA_ENG.ipynb
```

Then run all cells (Kernel → Restart & Run All). Note that `marvel_full.csv` is large - the betweenness centrality and diameter computations on it can take several minutes.

## License

Academic project, submitted for the DAA course at ISCTE-IUL. Not licensed for reuse.