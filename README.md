# 🚓 Savior of the Louvre - Paris Police Chase Simulator

A dynamic, real-time police chase simulator built using graph algorithms to simulate a thrilling pursuit through the streets of Paris after a daring art heist at the Louvre Museum.

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📖 Overview

This project simulates an exciting chase scenario where burglars (Car A) attempt to escape through Paris streets while police (Car B) pursue them. The simulation uses Dijkstra's algorithm for pathfinding and incorporates dynamic events like traffic jams, road blockages, and one-way restrictions that force both vehicles to constantly replan their routes.

### ✨ Key Features

- **Custom Dijkstra Implementation**: Shortest path algorithm implemented from scratch
- **Two-Car Simulation**: Burglar car vs. Police car with different speeds and objectives
- **Dynamic Events System**: Random traffic jams, blockages, and one-way restrictions
- **Real-time Path Replanning**: Both cars adapt their routes based on changing conditions
- **Intelligent Pursuit**: Police car continuously tracks and chases the burglar's position
- **Rich Visualization**: NetworkX-based graph visualization with matplotlib
- **Detailed Simulation Logs**: JSON output for analysis and replay

## 🎯 Simulation Rules

### Car A (Burglars)
- **Start Position**: Node 0
- **Speed**: 1.0 units per timestep
- **Objective**: Reach exit node 48 as fast as possible
- **Replanning**: Only when dynamic events affect the route

### Car B (Police)
- **Start Position**: Node 49
- **Delay**: 3 timesteps before starting
- **Speed**: 1.5 units per timestep (50% faster!)
- **Objective**: Catch Car A before it reaches the exit
- **Replanning**: Continuous tracking - replans after each node or event

### Dynamic Events
| Event Type | Effect | Duration |
|-----------|--------|----------|
| **Traffic Jam** | Multiplies edge weight by 2.0-2.5x | 3 steps |
| **Blockage** | Temporarily removes edge | 4 steps |
| **One-way** | Removes reverse direction | 6 steps |

*Probability*: 30% chance per timestep

## 🛠️ Tech Stack

- **Python 3.8+**
- **NetworkX**: Graph creation and manipulation
- **Matplotlib**: Static visualization
- **Copy**: Deep copying for event management
- **JSON**: Data storage and configuration
- **Heapq**: Priority queue for Dijkstra's algorithm

## 📦 Installation

### Prerequisites

