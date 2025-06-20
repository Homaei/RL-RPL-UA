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
@inproceedings{homaei2025rlrplua,
  author    = {Homaei, Mohammadhossein and Tarif, Mehran and Di Bartolo, Agustin and Ávila Vegas, Mar},
  title     = {A Reinforcement Learning-Based Telematic Routing Protocol for the Internet of Underwater Things},
  booktitle = {Proc. XVII Jornadas de Ingeniería Telemática (JITEL)},
  year      = {2025},
  address   = {Cáceres, Spain},
  month     = {November}
}

