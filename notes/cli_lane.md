# Command-line check

Fill during prework or the Slot 1 pause (Thu 10:35–10:45).

## Command run

```text
claude --version
# the desktop app's bundled claude.exe, run by its full path
& $env:CLAUDE_CODE_EXECPATH --version
```

## Result

- Exit / version string: `2.1.330 (Claude Code)` from the desktop app's bundled executable (checked 2026-11-26, Windows 11). The variable above is set inside the agent's session.
- Working directory: repository root (`ac4e-eief-workshop`)
- Tool: Claude Code (desktop app, Code tab)

## Blocker (if any)

What failed and what you will try next. Do not paste secrets.

- `claude` is not available as a terminal command. Claude Code runs through the desktop app, so the separate command-line install (`SETUP.md` section 5) was skipped.

Other setup results (2026-11-26):

- `pip install -r requirements-lock.txt` first failed on Python 3.11.14 (`contourpy==1.4.0` requires Python 3.12 or later). After installing Python 3.12.10 and rebuilding `.venv`, the locked requirements installed.
- `python -m pytest examples/card-krueger-toy/tests examples/mini-economics/tests` (in `.venv`): 45 passed.
- `python scripts/validate_setup.py` (in `.venv`): exit 0, no required item missing. It warned that `code` exists but failed to launch from the script; `code --version` run directly prints 1.146.0.

## Link forward

Slot 2 runs the `replication-checker` Skill from this tool, or from its app.
