---
layout: post
title: SIAM Travel Award and SIAM PP'16
modified:
tags: [intro, beginner, jekyll, tutorial]
comments: true
---

I have recently received the wonderful news that I have been granted the **SIAM Travel Award** for participating at the
**SIAM Conference on Parallel Processing for Scientific Computing (SIAM PP'16)** in Paris, and presenting my work on
**parallel sparse Tucker tensor decompositions**. 
In addition, there will be numerous presentations involving parallelization issues in various problem domains, and I
will have the chance to attend some of these interesting talks. 
My talk will specifically be at the **Salle des Theses** on **April 14, Thursday** at **2:40PM**.

In the talk, I will present the parallelization of the **Higher Order Orthogonal Iteration (HOOI)** algorithm which involves 
tensor-times-matrix multiply and truncated SVD steps.
Specifically, I will explain how to perform the expensive tensor-times-matrix multiply (TTM) operations in a
**communication avoiding** manner where we increase the total amount work in order to asymptotically reduce the
communication requirements.
Using this technique, our code graciously **scales up to 4096 cores** on an IBM BlueGene/Q machine using real-world tensors
having **over 100M nonzeros**, which enables us to perform Tucker analysis on such big tensors in the order of seconds.
