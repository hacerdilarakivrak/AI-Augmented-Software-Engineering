# Lab 3 Submission: A Mini Coding Agent

**Student:** Hacer Dilara Kivrak

**Project Repository:** https://github.com/hacerdilarakivrak/lab3-mini-coding-agent

## Project Summary

I implemented a mini coding agent using Python, Ollama, and the `llama3.1:8b` language model.

The agent includes three tools:
- `list_files`
- `read_file`
- `run_tests`

## Safety Features

- File access is restricted to the project directory.
- Running tests requires user approval.
- The agent loop is limited to 20 steps.
- Unknown tool calls are rejected.

## Test Results

- File listing and reading: PASS
- User permission control: PASS
- Automated unit tests: 4/4 PASS
- Agent-executed unit tests: 4/4 PASS

The complete source code, `README.md`, tests, and `writeup.md` are available in the linked project repository.
