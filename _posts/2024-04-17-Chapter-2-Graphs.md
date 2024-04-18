---
layout: post
title: Chapter 2 Graphs
date: 2024-04-17 21:34:34
description: SCM is built upon a graph
tags: causality
categories: sample-posts
---

**Definition.**(Graphs) A graph $$\mathcal{G} = (\mathbf{V}, \mathbf{E})$$ consists of finitely many nodes $$V$$ and edges $$\mathbf{E} \subseteq \mathbf{V} \times \mathbf{V}\ \forall v \in\mathbf{V}, (v,v) \notin E$$. We mostly work with directed graphs, i.e., $$(v,w) \in \mathbf{E} \Rightarrow (w,v) \notin \mathbf{E}$$.


- **path**
  
  > A sequence of vertices connected by edges, e.g. $$A\rightarrow B\leftarrow C\rightarrow D$$
  
- **collider on a path**
  
  > A specific configuration on a path where two arrows meet head-to-head at a vertex, e.g. $$B$$ is a collider on path $$A\rightarrow B\leftarrow C\rightarrow D$$ 
  
- **directed path (dir. path)**
  
  > A path where all the edges are directed in the same direction, e.g. $$E\rightarrow F\rightarrow G\rightarrow H$$
  
- **v-structure**
  
  > An arrangement of three variables where two have arrows directed towards the third and these two are not directly connected. For example, in causal graph $$A\rightarrow B\leftarrow C\rightarrow D$$, $$A\rightarrow B\leftarrow C$$ forms a v-structure. On the contrary, if $$A$$ and $$C$$ are directly connected in this causal graph, then $$A$$, $$B$$ and $$C$$ no longer form a v-structure.
  
- **directed cycle (dir. cycle)**
  
  > A path that starts and ends at the same vertex with all edges directed in a consistent direction.
  
- **directed acyclic graph (DAG)**
  > A graph with no directed cycles.

- **PA (Parents)**
  
  > For a vertex $$X$$ in a graph, its set of parents, denoted as $$PA_X$$, is the set of all vertices that have a direct edge leading to this vertex.
  
- **CH (Children)**
  > For a vertex $$X$$ in a graph, its set of children, denoted as $$CH_X$$, is the set of vertices that this vertex points to directly through outgoing edges.

- **DE (Descendants)**
  
  > For a vertex $$X$$ in a graph, its set of descendants, denoted as $$DE_X$$, includes all vertices that can be reached by following directed paths starting from this vertex
  
- **ND (Non-Descendants)**
  
  > For a vertex $$X$$ in a graph, its set of non-descendants, denoted as $$ND_X$$, is the set of vertices that are neither descendants nor the vertex itself.
  
- **AN (Ancestors)**
  
  > For a vertex $$X$$ in a graph, its set of ancestors, denoted as $$AN_X$$, includes all vertices from which there is a directed path leading to this vertex.

Given definitions above, in a graph $$\mathcal{G}=(\mathbf{V}, \mathbf{E})$$, for each vertex $$X\in\mathbf{V}$$, the set of vertices can be split into three disjoint subsets
$$
\mathbf{V} = ND_X\sqcup DE_X \sqcup \{X\},
$$
where $$\sqcup$$ means disjoint union. That is, for each vertex in a graph, the set of vertices is the disjoint union of its descendants, its non-descendants and itself.
