---
layout: post
title: MultiRepast4py
github: "https://github.com/KengLL/MultiRepast4py"
image: "/img/in-project/minds_lab.png"
tech:
  - name: "Repast4py"
    icon: "/img/tech/repast4py.jpeg"
  - name: "Python"
    icon: "/img/tech/python.png"
description: Developed MultiRepast4py, a framework extending Repast4py to enable multilayer agent-based simulations for analyzing complex, interconnected systems.
tags:
  - "Software Development"
  - Research
---

# Empowering Multilayer Simulations

### 1. **Introduction**  
MultiRepast4py is a Python package that extends the Repast4py agent-based simulation platform to support multilayer simulations.  

Humans naturally navigate multiple social identities (intersectionality)—we participate in workplaces, families, and various other networks simultaneously. Multilayer simulations capture these complex, interconnected interactions, enabling more accurate modeling of real-world dynamics.

![Concept of Edge storing](/img/in-project/multi_edge.jpeg)


## Key Achievements
**Enhanced Scalability**:
Increased simulation capacity by **100x** to support **50,000 agents per layer** on commercial edge devices. (Apple M2 chip, 8gb RAM)

**Innovative Data Management**:
Transitioned from traditional matrix-based edge storage to **decentralized per-agent edge lists**, ensuring efficient memory usage and easier manipulation of complex network interactions.

**User-Friendly Transition**:
Enabled a smooth upgrade from single-layer models with **minimal modifications**, complete with comprehensive documentation and demo examples.

**Recognized Excellence**:
Awarded the **SRIP scholarship**, presented at the **2024 UC San Diego Summer Research Conference**, and recognized as first author on a research paper submitted to **AAMAS 2025**.

## Technical Approach  
The core implementation of MultiRepast4py focuses on processing input files efficiently. Instead of relying on traditional adjacency matrices, we parse network files by extracting edges for each agent and storing them in dictionaries. This decentralized approach allows models to reconstruct network structures dynamically using built-in functions from the MultiRepast4py package. Additionally, helper functions are provided to simplify the agent construction process.  

## Impact & Recognition  
MultiRepast4py enables researchers to gain deeper insights into various domains, including public health policy, misinformation dynamics, and complex social behaviors.  

My primary focus is on misinformation. Growing up in a geopolitically tense region, I’ve witnessed how misinformation can threaten democratic discourse and social stability. I believe that fostering a safe environment for healthy discussions requires robust defenses against cyber threats, including misinformation campaigns. MultiRepast4py provides a framework to study these challenges and develop potential countermeasures.  

## How to Get Started  
A detailed tutorial is available on the [GitHub repository](https://github.com/KengLL/MultiRepast4py).  

This implementation is a direct extension of the **Rumor Model in Repast4py**, showcasing a clear and intuitive transformation into a multilayer simulation framework.  

## Acknowledgments  
Special thanks to the UCSD Summer Research Internship Program, NSF (Award CCF-2416311), and [MINDS Lab](https://parinazn.com/group/) for their support and the opportunity to pursue this research.  

![Photo with my PI, Parinaz Naghizadeh](/img/in-project/pi_photo.JPG)
## Additional Information  
- **Paper:** [AAMAS](https://github.com/KengLL/MultiRepast4py/blob/main/MultiRepast4py_MABS2025.pdf)
- **Video Presentation** [UCSD Summer Research Conference 2024](https://youtu.be/F-69nq532dU?si=SHQo6uecUbGGGi0H)
- **Future Work:** We plan to incorporate **data-driven features** and explore the integration of **intelligent agents powered by LLMs** to enhance the simulation capabilities.  