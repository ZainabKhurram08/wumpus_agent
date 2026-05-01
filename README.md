# Wumpus Logic Agent

A web-based Knowledge-Based Agent that navigates a Wumpus World grid using Propositional Logic and Resolution Refutation.

## Live Demo
[https://zainab00.pythonanywhere.com](https://zainab00.pythonanywhere.com)

## Features
- Dynamic grid sizing (any Rows x Columns)
- Random Wumpus and Pit placement each episode
- Propositional Logic Knowledge Base (TELL / ASK)
- Automated Resolution Refutation for safe cell inference
- Real-time metrics: Inference Steps, Moves, Safe Visited
- Percept display: Breeze and Stench
- Step-by-step mode

## How It Works
The agent maintains a KB of CNF clauses. When it enters a cell it receives percepts and TELLs the KB new rules. Before moving to any unvisited neighbor it ASKs the KB via Resolution Refutation : negating the query, adding it as a clause, and running the resolution loop. If the empty clause is derived, the cell is proven safe.

## Tech Stack
- Backend: Python, Flask
- Frontend: HTML, CSS, JavaScript
- Deployment: PythonAnywhere
