---
layout: post
title: Travel to Supercomputing `15
modified:
tags: [intro, beginner, jekyll, tutorial]
comments: true
---

Last April, after sustaining an inhumane effort of coding/testing/ debugging cycle for a couple of weeks, we managed to get some great speedup results for the first *communication optimal* parallelization of CP tensor factorization of sparse tensors, and submitted the first article of my PhD. thesis to the upcoming Supercomputing conference.
We got the wonderful news of the acceptence of our paper in June, which gave me the great apportunity to participate and present my work in one of the largest conferences in the field.

The very first step I will be taking in SC is attending the tutorial on advanced MPI techniques on Nov. 16, Monday.
I cannot wait to discover what is to come from this tutorial; as I am very positive about all these shiny-new advanced features, specifically neighbor collective communications, to overcome current performance barriers we face in HyperTensor.
Indeed, introducing hybrid parallelism is an effective way of improving the parallel performance, putting aside everything else, just by reducing the number of MPI ranks; thereby the total communication latency, which typically becomes the major communication bottleneck in parallel sparse irregular data-intensive methods (and tensor factorization is a canonical example of those, as I will discuss in my talk).
However, immediately after trying to employ this, I started to realize how difficult, and at times impractical, it could get to provide an efficient OpenMP parallelism to every single operation you do.

We already have a very effective hybrid parallelism for Tucker factorization, which gave us up to **700x** speedup over 2048 cores using 256 MPI ranks on real-world sparse tensors.
From a developer's perspective, a pure-MPI implementation using the advanced features is much more preferable to a hybrid parallelization approach; since, as also discussed by the *PETSc* team <a href="http://www.mcs.anl.gov/petsc/miscellaneous/petscthreads.html" class="textlink" target="_blank">here</a>, it provides a significantly simpler programming model, and is easier to develop, maintain, test, and even optimize than the hybrid approach.
However, I would like to wait and see how the performance of these two approaches compare at the end of the day.
I have my sincere hopes that pure-MPI 'magically' prevails, and I keep my fingers crossed on this.

My talk is titled 'Scalable Sparse Tensor Decompositions in Distributed Memory Systems' and is scheduled to take place **between 4:00--4:30PM on Thursday, November 19 in 18CD**.
As the title suggests, I will be presenting a full MPI parallelization of CP-ALS algorithm, show scalability results, and discuss the limiting factors towards further scalability.
Particularly, if you are interested in parallel sparse matrix kernels such as SPMV, I believe you will find my talk very interesting in the sense that many performance techniques, as well as limitations, from sparse matrix operations generalize to tensor computations.
For example, scalability limitations of parallel SPMV such as high communication latency apply to parallel sparse tensor factorization; albeit to a greater extent. In addition, graph and hypergraph partitioning can similarly be employed to tensor operations to grasp and reduce their communication cost metrics.

If you will be around at SC and share similar taste of research or find my work interesting in some way, I will be around! Please do not hesitate to contact me by e-mail so we might have a nice little talk over a coffee break while we are at it!

