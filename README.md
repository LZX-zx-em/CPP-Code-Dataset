# CPP-Code-Dataset
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20763753.svg)](https://doi.org/10.5281/zenodo.20763753)

A comprehensive C++ evaluation dataset comprising 200 multi-level samples (from basic structures to industrial applications) for benchmarking LLM code generation.

## Dataset Overview

**C++-Eval** is a comprehensive C++ evaluation dataset comprising 200 multi-level samples designed to assess the code generation capabilities of Large Language Models (LLMs) in high-performance, industrial scenarios. To address the limitations of existing benchmarks, this dataset covers six major engineering scenarios: basic data structures, classic algorithms, numerical computation, machine learning preprocessing, image and point cloud processing, and advanced object-oriented features. Furthermore, each task is accompanied by a complete set of function declarations and approximately 20 high-coverage test cases covering boundary conditions and exceptional scenarios to ensure rigorous evaluation.

## Dataset Statistics

- **200** multi-level C++ programming tasks, each with **~20** human-authored, high-coverage test cases (boundary inputs, invalid inputs, exception handling)
- **6 engineering scenarios**: basic data structures, classic algorithms, numerical computation, machine learning preprocessing, image and point cloud processing, and advanced object-oriented features
- **3 difficulty levels** (basic / intermediate / advanced), classified by cognitive complexity and lines of code (LoC)
- Coverage of core C++ features and paradigms: OOP, generic programming, explicit memory management, and modern C++11 mechanisms

## Data Structure

The dataset is structured in a `.jsonl` (JSON Lines) format, where each line represents a single C++ programming task. The primary fields in the dataset include:

* **`task_id`**: A unique identifier number for each evaluation task.
* **`question`**: The detailed task prompt provided to the LLM. This includes the required C++ function declarations, clear natural language descriptions, specifications of input and output formats, and necessary code comments.

## Construction & Decontamination

- Task concepts curated from public platforms (LeetCode, Codewars, GitHub), followed by semantic-based manual verification
- Interface contract and signature refactoring to break verbatim prompt matching against public repositories
- Execution-based decontamination: all solutions compiled with `g++ -std=c++11` and `-fsanitize=address` (AddressSanitizer) to capture low-level memory faults

## Evaluation Protocol

- Strict zero-shot prompting
- Metrics: task-level error probability, compilation success rate, and task-level pass rate, with 95% Wilson score confidence intervals

## Citation

Archived on Zenodo: https://doi.org/10.5281/zenodo.20763753
