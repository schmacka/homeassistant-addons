# Printernizer Slicer

OrcaSlicer-based slicing service for **Printernizer**. Runs in its own container
(multi-arch: works on Raspberry Pi / arm64 and amd64).

## Install
1. Install this add-on and start it. It serves a slicing API on port **8001**.
2. In the **Printernizer** add-on, set the slicer service URL to this add-on, e.g.
   `http://local-printernizer_slicer:8001` (the exact internal hostname is shown on
   this add-on's info page). Printernizer reads it as `SLICER_SERVICE_URL`, then
   auto-registers the slicer and seeds built-in profiles (Bambu A1, Prusa CORE One).

Verify on Printernizer: `GET /api/v1/slicing` should list one slicer.

Image: `ghcr.io/schmacka/printernizer-slicer` (pinned to the matching app version).
