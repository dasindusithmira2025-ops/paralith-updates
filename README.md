# PARALITH Updates

Public distribution for signed PARALITH updater artifacts and channel manifests.

This repository intentionally contains no application source, credentials, databases, or private diagnostics. Versioned installers and signatures are published as GitHub Release assets. A least-privilege GitHub Actions workflow validates staged publication batches and atomically activates channel manifests under `channels/`.
