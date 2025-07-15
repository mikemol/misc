# Active Research - Experiments & Findings

This document is a living log of ongoing experiments, analyses, and findings related to my various ML-related thoughts, the G-Calculus, and related topics in AI and ML. It serves as a record of active research, test results, and code development.  It is intended to provide a high-level view of research and to assist in the review.

## 1. Overview

*   **Purpose:** To document *active research* efforts, including:
    *   Experiment design and execution.
    *   Analysis of results.
    *   Code development progress.
    *   Open questions.
    *   Relevant projects.
*   **Organization:**  Organized by experiment, project, or research area. Each entry includes:
    *   Title.
    *   Date of entry.
    *   Brief Description.
    *   Key Findings or Progress.
    *   Relevant code snippets (with links to repositories or files).
    *   Open Questions and Next Steps.

## 2. Experiments and Projects

### 2.1. Experiment: Simple Dissonance Minimization in a Resistor Mesh (2024-07-26)

*   **Description:**  Simulating a simple resistor network implementing the G-Calculus, demonstrating the minimization of Dissonance.
*   **Goal:** Demonstrate that the system converges to a low-energy state, and that its behavior is consistent with the 1/x Inversion process.
*   **Setup:** A simple resistor mesh with 4 nodes (A, B, C, D) and predefined conductances representing relationships.  Introduce an initial "high-energy" state (dissonance) and observe the system's evolution.
*   **Key Findings/Progress:**
    *   Initial simulation results indicate convergence towards a stable state.
    *   Dissonance, as measured by the voltage differences, decreased over time.
    *   Detailed in `code/resistor_mesh_simulation.py` (See link below).
*   **Code:**
    *   [GitHub Repository: g-calculus-simulations](link-to-github-repo/g-calculus-simulations)
        *   File: `code/resistor_mesh_simulation.py` (Implementation of the resistor mesh simulation).
*   **Open Questions and Next Steps:**
    *   Investigate the effects of changing the resistance values on the convergence speed and stability.
    *   Add a component to implement the "inversion" process
    *   Extend to a higher-order example.
*   **Consider**: Code for the graphs that result from this simulation.

### 2.2. Project: Implementing the OLOG KERNEL (2024-07-20 - Ongoing)

*   **Description:** Developing a Python implementation of the OLOG KERNEL, a knowledge graph construction and reasoning engine.
*   **Goal:** To create a system capable of representing and evolving knowledge, applying the Derrida/Diogenes Engine.
*   **Progress:**
    *   Implemented basic graph data structures and operations.
    *   Implemented a rudimentary model of the conceptual change process.
    *   (See `code/olog_kernel.py`).
*   **Code:**
    *   [GitHub Repository: olog-kernel-implementation](link-to-github-repo/olog-kernel-implementation)
        *   File:  `code/olog_kernel.py` (Core KERNEL implementation)
        *   File: `code/examples.py` (Example graph structures and operations).
*   **Open Questions and Next Steps:**
    *   Implement the Derrida/Diogenes Engine's logic (identifying dissonance and synthesizing new concepts).
    *   Integrate with the G-Calculus (if possible).
    *   Develop a user interface to visualize and interact with the knowledge graph.

### 2.3. Analysis: Revisiting the SRO-V Simplex within a Monoidal Dagger Category (2024-07-15)

*   **Description:** A theoretical exploration of the SRO-V simplex within a symmetric monoidal dagger category. Exploring the formalisms within this context.
*   **Goal:** To rigorously formalize the relationship of the vertices.
*   **Progress:**  Formalized the pushout construction of the *SRO-V Simplex*.
*   **Key Findings/Progress:**
    *   Identified the algebraic structure (the group of operations.)
    *   Developed the mathematical tools to manipulate these relationships.
*   **Code:**
    *   (Not applicable - this is a theoretical analysis)
*   **Open Questions and Next Steps:**
    *   Explore the implications of these observations for the other concepts.
    *   Build a *formal* representation of this structure that is verified with a theorem prover.

### 2.4. Example: Applying G-Calculus to an Abstract Problem

*   **Description:** Working through examples.
*   **Goal:**  To ensure the theory is predictive and correct.
*   **Progress:**  A problem.
*   **Key Findings/Progress:**
    *   (Add details, figures, and diagrams of your observations)
*   **Code:**
    *   [GitHub Repository: g-calculus-simulations](link-to-github-repo/g-calculus-simulations)
        *   File: `code/example_problem_analysis.py`
*   **Open Questions and Next Steps:**
    *   (Add details)

## 3. Tools and Technologies

*   **Python:**  Primary programming language.
*   **NumPy, SciPy:** Numerical computation and scientific computing libraries.
*   **Category Theory Libraries:** (Specify any libraries you plan on using).
*   **Diagramming Tools:** (Mention any tools for creating diagrams).
*   **Theorem Provers:** (If applicable, e.g., Lean, Coq).

## 4. Glossary of Terms

*   (Define key terms and abbreviations here to ensure consistency)

## 5. References

*   (Add citations to relevant sources here)
