# Mother Dairy Cold Chain Network Optimization

Scenario-based optimization and simulation of a multi-stage cold chain network for Mother Dairy using Python, Mixed Integer Linear Programming (MILP), simulation, AnyLogistix, and supply chain analytics.

## Project Overview

This academic Supply Chain Analytics project evaluates the design and feasibility of a national cold chain network for Mother Dairy under realistic capacity, demand, transportation, and cold-chain constraints.

The study addresses a key strategic question: whether Mother Dairy's existing processing network can support national demand, and how planned future facilities and strategically located distribution centres (DCs) can improve network feasibility, service levels, and resilience.

The project also evaluates the potential for selective exports of value-added dairy products as a secondary strategic opportunity enabled by improved logistics feasibility.

## Objectives

- Evaluate the feasibility of the existing Mother Dairy processing network.
- Identify strategically suitable distribution centre locations.
- Compare the existing network with an expanded network including future processing plants.
- Optimize plant-to-DC-to-market flows under capacity and cold-chain constraints.
- Evaluate operational performance under demand variability.
- Assess supply chain resilience under a prolonged distribution disruption.
- Translate analytical results into strategic and managerial recommendations.

## Methodology

The study combines prescriptive and predictive supply chain analytics through four major components:

### 1. Greenfield Analysis

A Python-based Mixed Integer Linear Programming (MILP) model was used to determine suitable DC locations and transportation flows.

The model considers:

- Facility opening decisions
- Plant and DC capacities
- Transportation costs
- Geographic distances
- Cold-chain feasibility
- Product flows from plants → DCs → markets

Two network scenarios were evaluated:

- **Baseline:** Existing processing plants only
- **Future:** Existing + planned future processing plants

### 2. Network Optimization

The optimization model evaluates binary facility-selection decisions and continuous transportation flows while minimizing total network cost subject to operational and cold-chain constraints.

### 3. 365-Day Simulation

A time-based simulation was used to evaluate network performance under demand variability.

The simulation tracks:

- Daily demand
- Inventory levels
- Stockouts
- Service levels
- Replenishment lead times

A Min–Max inventory policy and a 3-day replenishment lead time were incorporated.

### 4. Risk & Disruption Analysis

A 60-day disruption scenario was evaluated in which a major distribution centre could not receive replenishment.

This was used to assess the network's resilience and potential demand-fulfilment impact during prolonged operational disruptions.

## Key Assumptions

- Transportation costs are distance-based.
- Geographic distances are calculated using the Haversine method.
- Maximum cold-chain transport distance:
  - Milk: **500 km**
  - Fruits & Vegetables: **800 km**
- Target service level: **100%**
- Inventory policy: **Min–Max**
- Replenishment lead time: **3 days**
- Demand variability follows a normal distribution.

## Key Results

| Scenario | Result |
|---|---|
| Existing plants only | **Infeasible** |
| Average DC-to-market distance – baseline | **~721 km** |
| Existing + future plants | **Optimal** |
| Selected DCs | **Lucknow, Patna, Indore, Hyderabad** |
| Average DC-to-market distance – future network | **~389 km** |
| Normal simulation service level | **100%** |
| Temporary stockout events | **6** |
| Disruption scenario service level | **86%** |
| Demand unmet under disruption | **~14%** |

The results indicate that the existing network is structurally insufficient to satisfy national demand under the defined cold-chain and capacity constraints.

The inclusion of future processing plants enables an optimized regional distribution structure with four strategically located DCs.

## Strategic Insights

The analysis supports the following strategic recommendations:

1. Proceed with planned future processing plants because the existing network is structurally infeasible.
2. Adopt a regionalized distribution strategy using strategically positioned DCs.
3. Incorporate cold-chain constraints directly into strategic network design decisions.
4. Strengthen resilience through multi-sourcing and DC redundancy.
5. Explore selective exports of value-added and storable dairy products only after domestic demand is adequately served.

Potential export categories identified in the study include:

- Skimmed Milk Powder
- Ghee and butter oil
- Cheese and processed dairy products

Liquid milk exports were not considered practical or recommended because of perishability and logistical constraints.

## Tools & Technologies

- **Python**
- **Mixed Integer Linear Programming (MILP)**
- **Jupyter Notebook**
- **scikit-learn**
- **AnyLogistix**
- **Supply Chain Analytics**
- **Network Optimization**
- **Simulation Modelling**
- **Risk & Disruption Analysis**

## Repository Structure

```text
Mother-Dairy-Cold-Chain-Network-Optimization/
│
├── data/
│   ├── MD_GFA_AnyLogistix_Model.xlsx
│   ├── Mother_Dairy_Locations.xlsx
│   └── Mother_Dairy_Locations_v2.xlsx
│
├── docs/
│   └── TEAM-1_SCA_PROJECT.pdf
│
├── notebooks/
│   └── Mother_Diary.ipynb
│
└── README.md
