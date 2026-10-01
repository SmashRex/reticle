### Fixed

- @reticlehq/server: reticle kill --force could report success on Windows while a daemon was still running because lsof was unavailable. The daemon status now exposes its PID so the CLI can identify and terminate it without lsof, and kill now verifies that the port is actually free before reporting success. Closes #1243.