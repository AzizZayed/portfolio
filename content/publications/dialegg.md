---
title: 'DialEgg: Dialect-Agnostic MLIR Optimizer using Equality Saturation with Egglog - CGO 2025'
summary: 'MLIR’s ability to optimize programs at multiple levels of abstraction is key to enabling domain-specific optimizing compilers. However, expressing optimizations remains tedious. Optimizations can interact in unexpected ways, making it hard to unleash full performance.
 
Equality saturation promises to solve these challenges. First, it simplifies the expression of optimizations using rewrite rules. Secondly, it considers all possible optimization interactions, through saturation, selecting the best program variant. Despite these advantages, equality saturation remains absent from production compilers such as MLIR.
 
This paper proposes to integrate Egglog, a recent equality saturation engine, with MLIR, in a dialect-agnostic manner. This paper shows how the main MLIR constructs such as operations, types or attributes can be modeled in Egglog. It also presents DialEgg, a tool that pre-defines a large set of common MLIR constructs in Egglog and automatically translates between the MLIR and Egglog program representations. Using a few use-cases, this paper demonstrates the potential for combining equality saturation and MLIR.'
ShowWordCount: false
ShowReadingTime: false
author: ["Abd-El-Aziz Zayed", "Christophe Dubach"]
tags: ["compilers", "optimization", "MLIR", 'equality saturation', 'egglog']
# date: "2024-11-04"
cover:
    image: 'publications/dialegg-arch-bg.svg'
editPost:
    disabled: true
---
MLIR’s ability to optimize programs at multiple levels of abstraction is key to enabling domain-specific optimizing compilers. However, expressing optimizations remains tedious. Optimizations can interact in unexpected ways, making it hard to unleash full performance.

Equality saturation promises to solve these challenges. First, it simplifies the expression of optimizations using rewrite rules. Secondly, it considers all possible optimization interactions, through saturation, selecting the best program variant. Despite these advantages, equality saturation remains absent from production compilers such as MLIR.

This paper proposes to integrate Egglog, a recent equality saturation engine, with MLIR, in a dialect-agnostic manner. This paper shows how the main MLIR constructs such as operations, types or attributes can be modeled in Egglog. It also presents DialEgg, a tool that pre-defines a large set of common MLIR constructs in Egglog and automatically translates between the MLIR and Egglog program representations. Using a few use-cases, this paper demonstrates the potential for combining equality saturation and MLIR.

[PDF](/publications/zayedcgo24.pdf) [Slides]() [Artifact](https://github.com/AzizZayed/dialegg-cgo-artifact)