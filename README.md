# Service Network Design Model for Freight on Transit (SND-FOT)

Welcome to the GitHub repository for the Service Network Design for Freight on Transit (SND-FOT) model. This repository contains the implementation of a service network design model tailored to optimize the routing and transit of freight using a time-expanded network approach. Below is a brief overview of the model's structure, the variables involved, and the objective it seeks to achieve.

## Model Overview

The SND-FOT model is a mathematical framework designed to optimize freight transportation within a network of transit lines and hubs. This model aids in deciding the most efficient routes for freight vehicles and the allocation of freight across the network, focusing on maximizing the utilization of the network and minimizing the costs associated with freight transit.

### Variables

- **Binary Variable \(x^{k,t\overline{t}}_{ij}\):** Indicates whether a freight request \(k\) is transported on the arc from node \(i\) at time \(t\) to node \(j\) at time \(\overline{t}\).
- **Integer Variable \(y^{k,t\overline{t}}_{ij}\):** Represents the number of freight vehicles used on the arc from node \(i\) at time \(t\) to node \(j\) at time \(\overline{t}\).
- **Binary Variable \(z_r\):** Signifies if transit line \(r\) is utilized in the network.
- **Binary Variable \(s_k\):** Represents whether commodity \(k\) is serviced within the network.

### Model Versions

Three versions of the model are provided, each varying in complexity:

1. **Uncapacitated Model (USND-FOT):** This simplified version ignores capacity constraints on network facilities and links, enabling a more manageable and quicker solution process. It is focused on evaluating decisions related to the selection of transit routes and the number of hubs that can be handled efficiently.

2. **Capacitated Model with Terminal Constraints:** Introduces capacity constraints at transit terminals to reflect limitations in freight handling and storage, critical due to the movement of both passengers and freight in shared spaces.

3. **Fully Capacitated Model:** Extends the capacity constraints to all nodes in the network, including transit and hub nodes, and limits the number of vehicles that can operate, providing a comprehensive view of network capabilities.

### Objective

The model seeks to maximize profits by serving the highest number of commodities while minimizing the associated transportation costs. This is achieved by optimizing the dispatching of trucks between hubs, reducing the cost of utilizing transit routes, and maximizing the number of commodities served.

### Mathematical Formulation

The objective function and constraints of the model are designed to:

- Maximize the number of commodities served and the profit generated.
- Minimize the costs for dispatching trucks and utilizing transit routes.
- Enforce flow conservation, ensuring commodities move from origin to destination nodes correctly.
- Convert commodity-arc movements to truck-arc movements.
- Select appropriate transit routes based on schedule and availability.
- Maintain the domain and integrity of decision variables.

### Applications

The SND-FOT model can be used by researchers and practitioners in logistics and transportation to:

- Explore various network configurations and their impact on freight transit efficiency.
- Develop and test algorithms for solving network design problems.
- Analyze the scalability of uncapacitated and capacitated models.

For more details on the implementation and usage of the model, please refer to the included documentation and examples in this repository.
