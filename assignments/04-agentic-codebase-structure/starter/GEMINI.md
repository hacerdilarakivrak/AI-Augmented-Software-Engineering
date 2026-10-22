# GEMINI.md

For complete repository guidance, architecture, and workflows, please read [AGENTS.md](./AGENTS.md).

## Scoped Testing Instructions (`test_main.py`)
Because existing tests reside in root `test_main.py` rather than a `tests/` subdirectory, path-scoped subfolder instructions (`tests/GEMINI.md`) do not automatically apply here. When working on test files (`test_main.py`), explicitly load and adhere to the testing standards outlined in [AGENTS.md](./AGENTS.md) and run `pytest` to validate behavioral tests.
