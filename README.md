# Tail-Aware-Sparse-FCP

**Overview**

This project implements a communication-efficient method for federated conformal prediction using tail-aware sparse quantile aggregation.

In federated settings, data is distributed across multiple clients, making it difficult to compute the global conformal threshold. This project proposes a one-shot approach where each client sends a small number of quantiles focused on the upper tail of the distribution, enabling accurate uncertainty estimation with minimal communication.

**Key Idea**

Instead of uniformly summarizing the entire distribution, we focus on the region that matters most for conformal prediction:

q∗=Q_1−α
	​
**Method:**
Tail-aware quantile selection

Clients compute quantiles concentrated near 1−α

Sparse communication

Each client sends only a few quantiles

Robust aggregation

Server aggregates using median (to handle heterogeneity)

Interpolation

Estimate the global threshold via interpolation

**Features**

Tail-aware quantile grid

One-shot federated aggregation

Robust (median-based) aggregation

Low communication cost

Works under heterogeneous client distributions

**Experiments**

We evaluate the method under:

Homogeneous clients

Heterogeneous clients (shifted + scaled distributions)
