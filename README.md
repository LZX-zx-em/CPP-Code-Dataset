# CPP-Code-Dataset
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20763753.svg)](https://doi.org/10.5281/zenodo.20763753)
A comprehensive C++ evaluation dataset comprising 200 multi-level samples (from basic structures to industrial applications) for benchmarking LLM code generation.
## Dataset Overview
**C++-Eval** is a comprehensive C++ evaluation dataset comprising 200 multi-level samples designed to assess the code generation capabilities of Large Language Models (LLMs) in high-performance, industrial scenarios. To address the limitations of existing benchmarks, this dataset covers six major engineering scenarios: basic data structures, classic algorithms, numerical computation, machine learning preprocessing, image and point cloud processing, and advanced object-oriented features. Furthermore, each task is accompanied by a complete set of function declarations and approximately 20 high-coverage test cases covering boundary conditions and exceptional scenarios to ensure rigorous evaluation. 

## Data Structure
The dataset is structured in a `.jsonl` (JSON Lines) format, where each line represents a single C++ programming task. The primary fields in the dataset include:

*   **`task_id`**: A unique identifier number for each evaluation task.
*   **`question`**: The detailed task prompt provided to the LLM. This includes the required C++ function declarations, clear natural language descriptions, specifications of input and output formats, and necessary code comments.
