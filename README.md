# Reasoning Prompt Condition Analysis

This notebook investigates whether an open-weight language model produces consistent answers to reasoning problems across three prompt conditions: clean, subtly hinted (toward the correct answer), and misleadingly hinted (toward an incorrect answer).

## Motivation

A core challenge in evaluating reasoning models is distinguishing genuine reasoning from shortcut-driven behaviour. A model that arrives at the correct answer under clean conditions may be doing something entirely different internally when surface cues are present. This notebook is a small empirical exploration of that question.

## What This Notebook Does

- Loads Qwen2.5-0.5B-Instruct, an open-weight instruction-tuned language model
- Constructs reasoning problems in three versions: clean, subtly hinted, and misleadingly hinted
- Runs the model on all conditions and logs final answers and reasoning
- Saves results to a structured CSV for analysis

## Prompt Conditions

Each reasoning problem is written in three versions:
- **Clean**: No hints, just the problem as stated
- **Subtly hinted**: A nudge toward the correct answer embedded in the problem
- **Misleadingly hinted**: A nudge toward an incorrect answer embedded in the problem

## Results

Results are saved in `reasoning_results.csv` with columns: condition, prompt, response.

## Tech Stack

- Python
- HuggingFace Transformers
- PyTorch
- pandas
- Google Colab (T4 GPU)

## License

MIT
