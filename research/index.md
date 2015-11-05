---
layout: page
title: Research
date: {{ date }}
modified:
share: false
excerpt:
tags: [research]
image:
  feature:
---

### High Performance Parallel Sparse Tensor Computations

![Smithsonian Image]({{ site.url }}/images/cp.png){: .image-pull-right .image-inside}
Tensor factorization/decompositions are widely used in the literature to model, approximate, and compress high dimensional data for which low-rank assumptions hold.
Many high dimensional real-world data can be naturally expressed as a sparse tensor; thereby can be analyzed using tensor factorization.

I am particularly interested in providing high performance parallel sparse tensor factorization kernels to scale such analysis to thousands of processors.
I focus on shared and distributed memory parallel algorithms, tensor data structures for computational and memory efficiency, computational techniques to reduce the amount of required computations, and tiling, reordering, partitioning strategies to improve efficiency and scalability. In our recent work, we parallalized CANDECOMP/PARAFAC (CP) and Tucker decomposition algorithms, and achieved **up to 700x speedup** using 2048 cores.
We implemented these algorithms in our templated C++ library **HyperTensor**, which uses OpenMP and MPI for shared and distributed memory parallelism (will be available soon).

### Graph and Hypergraph Algorithms


