---
layout: post
title: MultiRepast4py
image: "/img/in-project/minds_lab.png"
tech:
  - name: "Repast4py"
    icon: "/img/tech/repast4py.jpeg"
  - name: "Python"
    icon: "/img/tech/python.png"
description: Developed MultiRepast4py, a framework extending Repast4py to enable multilayer agent-based simulations for analyzing complex, interconnected systems.
---

# MultiRepast4py: Enabling Multilayer Agent-Based Simulations

## Overview
MultiRepast4py is a Python-based framework that extends Repast4py to support agent-based simulations on multilayer networks. This tool empowers researchers to model and analyze complex interactions across interconnected systems, such as multilayer social networks or multi-modal transportation systems, while maintaining scalability and efficiency.

---

## Introduction
Agent-Based Simulations (ABS) are a cornerstone for studying complex systems. Existing platforms like NetLogo and Repast are often limited to single-layer networks, failing to capture the nuances of multilayer interactions. MultiRepast4py addresses this gap by enabling simulations where agents operate across multiple interconnected networks, such as overlapping social media platforms or integrated transport systems.

---

## Features
- **Multilayer Simulation Capability**: Allows dynamic modeling of agents across multiple layers of interaction.
- **Scalability**: Built on Repast4py, leveraging MPI for distributed simulations, supporting large-scale models.
- **Ease of Use**: Minimal modifications required for integrating multilayer networks with existing single-layer models.
- **Customizability**: Compatible with Python libraries for data-driven and machine learning-enhanced ABS.

---

## Software Architecture
- **Framework**: Repast4py
- **Programming Language**: Python
- **Key Innovations**:
  - Multilayer network file parsing and reconstruction.
  - Efficient memory management with compression and encoding for network data.
  - Support for parallel agent initialization and execution.

**Image Slot**: Add a system diagram or architecture flowchart to visualize the multilayer simulation framework.

---

## Key Contributions
### 1. Multilayer Agent-Based Simulation Capability
MultiRepast4py enables researchers to simulate multilayer networks by seamlessly integrating inter-layer and intra-layer dynamics. This allows nuanced modeling of systems where multiple interaction modalities influence outcomes.

### 2. Efficient Memory and Parallel Processing
The framework introduces a decentralized data structure for agent attributes and employs compression techniques to optimize memory usage and performance for large-scale simulations.

### 3. Ease of Transition from Single-Layer Models
With minimal additional attributes and reconstruction of network data, researchers can adapt existing single-layer ABS models to the multilayer paradigm.

**Image Slot**: Include a simplified example of a multilayer network representation.

---

## Experimental Demonstration: Rumor Propagation
We demonstrated MultiRepast4py’s capabilities through a case study on rumor propagation across multilayer social networks.

### Simulation Setup
- **Network Topology**: Two-layer multiplex network with distinct social platforms modeled as Erdős–Rényi graphs.
- **Agent State Model**:
  - `received_rumor`: Binary state tracking rumor spread.
  - `shadow_data`: Multilayer adjacency list for network connections.
- **Simulation Protocol**: Monte Carlo simulations with 2,500 runs, analyzing propagation dynamics influenced by cross-layer connectivity.

### Findings
- Cross-platform connectivity significantly enhanced global propagation efficiency, surpassing single-layer analyses.
- Combined degree centrality emerged as a critical metric for optimizing diffusion strategies.

**Image Slot**: Add propagation results or comparative diffusion curves.

---

## Challenges and Solutions
### Challenges:
1. **Complexity of Multilayer Models**: Required efficient data structures for inter-layer and intra-layer interactions.
2. **Memory Overhead**: Storing large multilayer networks posed computational challenges.
3. **Real-Time Simulation Dynamics**: Incorporating dynamic interactions across layers required adaptive scheduling.

### Solutions:
1. Developed a unified representation for multilayer edges.
2. Compressed and encoded network data for efficient storage and access.
3. Leveraged Repast4py’s scheduling to enable dynamic layer-specific interactions.

**Image Slot**: Before-and-after performance comparison or memory optimization charts.

---

## Results
MultiRepast4py demonstrated:
- Scalability to 50,000 agents per layer with efficient execution on consumer-grade hardware.
- Enhanced prediction accuracy for complex systems like cross-platform information diffusion.

**Image Slot**: Add a final demonstration image or chart highlighting large-scale simulation results.

---

## Future Work
- Incorporating real-world data into simulations for data-driven ABS.
- Extending to support heterogeneous inter-layer interactions.
- Exploring integration with advanced visualization tools for multilayer networks.

---

## Conclusion
MultiRepast4py bridges the gap in ABS platforms by introducing robust multilayer simulation capabilities. It offers a powerful tool for researchers to explore complex systems with interconnected dynamics, paving the way for improved predictions and interventions.

---

**Acknowledgments**
Special thanks to the UCSD Summer Research Internship Program and NSF (Award CCF-2416311) for their support.
