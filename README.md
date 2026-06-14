# Kernel Engineer Roadmap
### Mohammad Abdurrehman Bhatti — NUTECH SE-2024
**From Student → x86 Assembly ML Kernels → CUDA GPU Kernels → Kernel Engineer**

---

## What This Is

This repository documents my complete journey from university student to kernel engineer — building everything from scratch, in public, one day at a time.

The goal is to become one of a globally rare class of engineers who can write optimized ML kernels in both x86-64 Assembly and CUDA. Most engineers with these skills have PhDs in computer architecture or systems. I am building it from consistency and curiosity.



---

## Roadmap at a Glance

| Phase | Focus | Duration | Milestone |
|-------|-------|----------|-----------|
| Phase 0 | Math + C Fundamentals | 3–4 months | Unshakeable foundation |
| Phase 1 | Core ML + NumPy from Scratch | 4–5 months | Neural net built by hand |
| Phase 2 | C Deep Dive | 6–8 weeks | Memory & systems mastery |
| Phase 3 | x86-64 Assembly + CPU Kernels | 4–5 months | Flagship portfolio project |
| Phase 4 | CUDA + GPU Kernels | 5–6 months | Kernel engineer level skills |





---

## Current Status

> 🟡 **Phase 0 — In Progress**

| Phase | Status |
|-------|--------|
| Phase 0: Math + C Fundamentals | 🟡 In Progress |
| Phase 1: Core ML + NumPy | ⬜ Not Started |
| Phase 2: C Deep Dive | ⬜ Not Started |
| Phase 3: x86-64 Assembly + CPU Kernels | ⬜ Not Started |
| Phase 4: CUDA + GPU Kernels | ⬜ Not Started |


---

## Flagship Projects

These are the proof-of-work projects that define this journey. Each one will have its own detailed README with benchmarks, implementation notes, and profiling results.

### 🔧 MNIST in x86-64 Assembly (Phase 3)
Architecture: `784 → 256 (ReLU) → 128 (ReLU) → 10 (Softmax)`  
AVX2 vectorized matrix multiply, trained with mini-batch SGD, callable from Python via ctypes.  
Target: >95% test accuracy.

### ⚡ CUDA Matrix Multiply Optimization Journey (Phase 4)
Six progressive versions from naive to Tensor Core accelerated.  
Target: 60–80% of cuBLAS performance.  
Profiled with NVIDIA Nsight Compute.

### 🔥 Simplified Flash Attention Kernel (Phase 4)
Tiled online softmax eliminating O(N²) memory complexity.  
Integrated as a custom PyTorch operator.

---

## Key Resources

| Resource | Phase | Link |
|----------|-------|------|
| 3Blue1Brown — Essence of Linear Algebra | 0 | YouTube |
| Andrej Karpathy — Neural Networks: Zero to Hero | 1 | YouTube |
| CS:APP — Bryant & O'Hallaron | 2–3 | Book |
| Godbolt Compiler Explorer | 2–3 | godbolt.org |
| Agner Fog Optimization Guides | 3–4 | agner.org |
| NVIDIA CUDA Programming Guide | 4 | docs.nvidia.com |
| Simon Boehm — CUDA Matmul Optimization | 4 | siboehm.com |

---

## Learning Notes

The `learning-notes/` folder contains a daily markdown file for every day of this journey — what I studied, what confused me, what clicked, what I want to revisit. It is a raw thinking record, not polished content.

If you want to follow the journey as it happens, that folder is the most honest place to look.

---

## Why This Exists

Most ML engineers use PyTorch and never look underneath it. A small number of systems engineers understand hardware but do not understand ML deeply. Almost nobody has both.

This roadmap builds both, from the ground up — the math, the C, the assembly, the CUDA

The goal is not to finish fast. The goal is to actually understand every layer of the stack.

---

*Started: 14 june 2026 | Expected Completion: ~24 months*  
*GitHub: [AbdurRehman-debug](https://github.com/AbdurRehman-debug)*
