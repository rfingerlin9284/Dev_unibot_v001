Wolfpack trading prototype

This repository contains the canonical wolfpack strategy prototype (regime-aware strategy packs and orchestrator).


Legacy code and duplicate artifacts have been archived to `legacy_leftovers/` and `archives/` and are excluded from this git repo.

To run locally:

```bash
python3 -m venv wolfpack_venv
source wolfpack_venv/bin/activate
pip install -r requirements.txt
python3 strategies/wolfpack_orchestrator.py
```

## Developer Quickstart

1. Create a python virtualenv and install deps:

```bash
./scripts/setup_dev.sh
source .venv/bin/activate
```

2. Copy env example and edit secrets:

```bash
cp env.example .env
# Edit .env to set any needed runtime and sandbox credentials
```

3. Run smoke checks and tests:

```bash
bash ./charter_check.sh
pytest -q
```

4. Run canary (stub):

```bash
./scripts/run_canary.sh
```

5. Promotion: use the GitHub Action `Promotion` (requires approval code).

Note: We run tests in two modes for comparison — once with no seed and once with `UNIBOT_SEED` set (see `scripts/test_both_modes.sh`). This helps detect issues that only appear under different randomness.


## Legacy READMEs moved (updated 20250922T153040)

No README files were moved.
