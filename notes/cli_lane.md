# Command-line check

Fill during prework or the Slot 1 pause (Thu 10:35–10:45).

## Command run

```text
claude --version
```

## Result

- Exit / version string: none; PowerShell reports that `claude` is not recognized as a command (checked 2026-11-26, Windows 11)
- Working directory: repository root (`ac4e-eief-workshop`)
- Tool: Claude Code (desktop app, Code tab)

## Blocker (if any)

What failed and what you will try next. Do not paste secrets.

- The `claude` command line was not found. Next: install it with `irm https://claude.ai/install.ps1 | iex` (`SETUP.md` section 5), open a new terminal and rerun `claude --version`. The desktop app is in use meanwhile.

Other setup results (2026-11-26):

- `pip install -r requirements-lock.txt` failed on Python 3.11.14: `contourpy==1.4.0` requires Python 3.12 or later. Installed from `requirements.txt` in `.venv` instead, so package versions are not the locked ones.
- `python -m pytest examples/card-krueger-toy/tests examples/mini-economics/tests` (in `.venv`): 45 passed.
- `python scripts/validate_setup.py` (in `.venv`): exit 0, no required item missing. It warned that `code` exists but failed to launch from the script; `code --version` run directly prints 1.146.0.

## Link forward

Slot 2 runs the `replication-checker` Skill from this tool, or from its app.
