# 📡 RL-RPL-UA: Reinforcement Learning-Based Telematic Routing for the Internet of Underwater Things

This repository accompanies the paper titled:

**"A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things"**  
📝 Presented at the XVII Jornadas de Ingeniería Telemática (JITEL 2025), Cáceres, Spain

## 📄 Abstract

The Internet of Underwater Things (IoUT) faces challenges such as high latency, limited bandwidth, and energy constraints. Traditional routing protocols like RPL fall short in such environments. This work introduces **RL-RPL-UA**, an enhanced RPL-based routing protocol that integrates a lightweight reinforcement learning (RL) agent within each node to adaptively select the best parent based on local metrics like energy, link quality, buffer occupancy, and delivery history. Simulation results demonstrate that RL-RPL-UA significantly improves delivery ratio, energy efficiency, and network lifetime in both static and mobile underwater scenarios.

## 🔍 Highlights

- ✅ Lightweight Q-learning agent embedded in each node  
- 📶 Dynamic parent selection based on local observations  
- 🧠 Adaptive Objective Function (OF) replaces static RPL metrics  
- 💡 Compatible with RPL control messages (DIO/DAO)  
- 📊 Outperforms UWF-RPL, Co-DRAR, UA-RPL, and UWMRPL in Aqua-Sim simulations


## 🔍 Highlights of background

| Protocol                   | RL   | RPL   | Adaptive OF        | Mobility | Citation        |
|----------------------------|------|-------|--------------------|----------|-----------------|
| C-GCo-DRAR                 | ❌   | ❌   | Static OF          | Limited  | Guo2023         |
| FLCEER                     | ❌   | ❌   | Static OF          | Moderate | Natesan2020     |
| IDA-OEP                    | ❌   | ❌   | Static OF          | Limited  | Wang2024        |
| GTRP                       | ❌   | ❌   | Static OF          | Moderate | Khan2021        |
| RL Protocol                | ✅   | ❌   | Static OF          | Moderate | Eris2024        |
| Q-Learning                 | ✅   | ❌   | Dynamic OF         | Moderate | Nandyala2023    |
| Multi-agent RL             | ✅   | ❌   | Static OF          | High     | Li2020          |
| UA-RPL                     | ❌   | ✅   | Static OF          | Moderate | Liu2022         |
| URPL                       | ❌   | ✅   | Dynamic OF         | Moderate | Tarifdm2024     |
| Fuzzy-CR                   | ❌   | ✅   | Decision Making    | Moderate | Tariffuzzy2024  |
| UWF-RPL                    | ❌   | ✅   | Static Fuzzy OF    | Moderate | Tarif2025       |
| UW/MRPL (prev. work)       | ❌   | ✅   | Static OF          | High     | Homaei2025      |
| **RL-RPL-UA (this work)**  | ✅   | ✅   | **Dynamic**        | High     | —               |








## 📊 Simulation Results (Aqua-Sim / NS-2)

| Metric | RL-RPL-UA vs Baselines |
|--------|-------------------------|
| Packet Delivery Ratio | +9.2% over UWRPL |
| Energy per Packet | −14.8% energy use |
| Network Lifetime | +80 seconds |
| Routing Overhead | 45% lower |
| End-to-End Delay | 10–25% reduction |

## 🧠 Protocol Architecture

Each node includes:
- Sensing Unit
- RL Agent (Q-learning)
- Extended RPL Stack
- Acoustic MAC (TDMA)

Decision process modeled as an MDP with custom reward:

![Reward function](https://latex.codecogs.com/png.image?\dpi{110}&space;r_t=\alpha\cdot\text{PDR}_t-\beta\cdot\text{Delay}_t-\gamma\cdot\text{EnergyCost}_t)

---


## 📁 Repository Contents

- `RL-RPL-UA.tex` – Full LaTeX source of the manuscript
- `figures/` – Static and mobile simulation graphs (PDR, delay, energy, lifetime)
- `aqua-sim-scenarios/` – NS-2 / Aqua-Sim configuration files
- `readme/` – Abstract, key tables, and citation formats

## 📚 How to Cite This Work

### 📌 APA (7th Edition)

Homaei, M., Tarif, M., Di Bartolo, A., & Ávila Vegas, M. (2025). *A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things*. JITEL 2025.

---

### 📌 IEEE

M. Homaei, M. Tarif, A. Di Bartolo, and M. Ávila Vegas, “A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things,” in *Proc. XVII Jornadas de Ingeniería Telemática (JITEL 2025)*, Cáceres, Spain, Nov. 2025.

---

### 📌 BibTeX
```bibtex
@misc{homaei2025rlrplu,
  doi = {10.48550/ARXIV.2506.00133},
  url = {https://arxiv.org/abs/2506.00133},
  author = {Homaei,  Mohammadhossein and Tarif,  Mehran and Di Bartolo,  Agustin and Gutierrez, and Avila,  Mar},
  keywords = {Networking and Internet Architecture (cs.NI),  Artificial Intelligence (cs.AI),  Machine Learning (cs.LG),  FOS: Computer and information sciences,  FOS: Computer and information sciences},
  title = {A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things},
  publisher = {arXiv},
  year = {2025},
  copyright = {Creative Commons Attribution Share Alike 4.0 International}
}
```
---
```bibtex
@inproceedings{homaei2025rlrplua,
  author    = {Homaei, Mohammadhossein and Tarif, Mehran and Di Bartolo, Agustin and Ávila Vegas, Mar},
  title     = {A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things},
  booktitle = {Proc. XVII Jornadas de Ingeniería Telemática (JITEL)},
  year      = {2025},
  address   = {Cáceres, Spain},
  month     = {November}
}

