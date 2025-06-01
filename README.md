# Global Airline Network Analysis

A comprehensive analysis of the global flight network using graph theory, optimization, dynamic programming, and machine learning techniques. Built as part of the Computational Finance and Algorithms (CFA) course at Purdue University (MGMT 59000 – Spring 2025).

## Dataset

Sourced from [OpenFlights.org](https://openflights.org/data.html), combining:
- **Airports Dataset**: Metadata for 7,000+ airports including location, altitude, and time zones.
- **Routes Dataset**: 60,000+ airline routes with airline/operator info and airport pairs.

## Business Problem

Airline networks are complex systems requiring optimization for profitability, coverage, and efficiency. We asked:
- Which airports are truly central to global connectivity?
- Can we optimize routes to minimize cost while maximizing coverage?
- How can airlines make data-driven infrastructure and route decisions?

## Techniques Applied

Our work integrates at least 5 techniques from 3+ CFA categories, as required by the course:

| Technique                     | Category              | Purpose                                                  |
|------------------------------|------------------------|----------------------------------------------------------|
| Degree Centrality            | Graph Algorithms       | Identify busiest airports by direct connections          |
| Dijkstra's Algorithm         | Graph Algorithms       | Compute shortest-distance flight paths                   |
| Betweenness Centrality       | Graph Algorithms       | Identify strategic transfer hubs                         |
| Dynamic Programming (Bitmask)| Dynamic Programming    | Maximize distinct stops under a time budget              |
| Integer Linear Programming   | Optimization           | Select routes to cover key hubs                          |
| Spectral Clustering          | Machine Learning       | Detect regional clusters/communities                     |
| Minimum Spanning Tree        | Graph Algorithms       | Construct global connectivity backbone                   |

## Key Insights

1. **Busiest Airports**  
   Frankfurt, Paris (CDG), and Amsterdam are Europe's most connected hubs. Airlines can target these nodes for strategic interline partnerships and feeder routes.

2. **Shortest Path Routes**  
   Dijkstra’s algorithm reveals minimal legs like Frankfurt → Amsterdam (367 km), ideal for express service bundling and yield management.

3. **Hidden Global Hubs**  
   Anchorage and Keflavik emerged as vital transfer points based on betweenness, despite low traffic — highlighting overlooked strategic infrastructure.

4. **Optimized Itinerary**  
   A dynamic programming solution builds a 48-hour multi-continent route touching 11 cities — great for time-sensitive logistics or charter planning.

5. **Route Selection Model**  
   Integer programming shows that with just 100 routes, we can hit over 75% of top global hubs — optimizing efficiency for low-cost or new carriers.

6. **Community Clusters**  
   Spectral clustering identified 8 network regions (e.g., Arctic, Canada, Europe) — useful for alliances, route bundling, and regional aircraft deployment.

7. **Country-Level MST**  
   A minimum-cost global air backbone was built using MST, revealing robust bilateral links (e.g., Qatar–Bahrain) for cross-border coordination.

## Tools & Libraries

- Python (Jupyter Notebook)
- `networkx` – Graph algorithms
- `scikit-learn` – Spectral Clustering
- `numpy`, `pandas` – Data processing
- `PuLP` – Linear/Integer Programming
- `matplotlib` – Visualizations

## Files Included

- `CFA_Final_Project.ipynb` – Full analysis code
- `CFA_Project.docx` – Project report with all insights

