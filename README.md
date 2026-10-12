Software engineer focused on software systems, full-stack products, and real-time / 3D tooling. Shipping production apps and pipelines; aviation visualization is one domain I apply those skills to.

**[Geoknoesis](https://github.com/2eezy77)** · **[Public work](https://github.com/2eezy77?tab=repositories)**

### Language mix

| Language | Focus |
| --- | --- |
| **Python** | Pipelines, Flask apps, OpenUSD / Maya tooling |
| **JavaScript** | CesiumJS viz (HTML client; no TypeScript in public repos) |
| **C** | Parallel systems (MPI / OpenMP / Pthreads) |
| **SQL** | SQLite-backed Flask app data |

### Featured builds

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/window-hints">
        <img src="https://raw.githubusercontent.com/2eezy77/window-hints/main/docs/overlay-google.jpg" alt="window-hints" width="100%" />
      </a>
      <br />
      <strong>systems tooling</strong> · <b><a href="https://github.com/2eezy77/window-hints">window-hints</a></b><br />
      Systems tooling for Windows - UI Automation scan, overlay codes, hotkey cursor jumps.
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/openusd-live-control">
        <img src="https://raw.githubusercontent.com/2eezy77/openusd-live-control/master/docs/viewport.jpg" alt="OpenUSD Live Control" width="100%" />
      </a>
      <br />
      <strong>realtime 3D</strong> · <b><a href="https://github.com/2eezy77/openusd-live-control">openusd-live-control</a></b><br />
      Real-time 3D tooling - Maya / OpenUSD control via CLI to socket bridge to viewport.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/kiad-atc">
        <img src="https://raw.githubusercontent.com/2eezy77/kiad-atc/main/docs/kiad-atc-ui.jpg" alt="Real-time aviation visualization" width="100%" />
      </a>
      <br />
      <strong>geospatial viz</strong> · <b><a href="https://github.com/2eezy77/kiad-atc">kiad-atc</a></b><br />
      Real-time geospatial viz - CesiumJS, Photorealistic 3D Tiles, live ADS-B pipeline, overlay UI.
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/omniverse-integration">
        <img src="https://raw.githubusercontent.com/2eezy77/omniverse-integration/main/docs/architecture.jpg" alt="Omniverse Integration" width="100%" />
      </a>
      <br />
      <strong>3D ontology</strong> · <b><a href="https://github.com/2eezy77/omniverse-integration">omniverse-integration</a></b><br />
      Semantic 3D pipeline - bidirectional USD / glTF / FBX / CityGML conversion for Omniverse.
    </td>
  </tr>
</table>

Also shipping: [stem-summer-camp-registration](https://github.com/2eezy77/stem-summer-camp-registration) · [csci320-parallel-programming-portfolio](https://github.com/2eezy77/csci320-parallel-programming-portfolio)

Also live: [monterorentals.com](https://www.monterorentals.com) (rental product; source is not in the public repo list).

### How to run the public work

Verified against each repo's README and source (2026-10-12). Full runbooks stay in those repos.

| Repo | Start here | Constraints |
| --- | --- | --- |
| [window-hints](https://github.com/2eezy77/window-hints) | `python -m pip install -r requirements.txt`, then `python -m multiwindow_ui_hints` | Windows. Elevate with `Run-UI-Hints.ps1` for hints inside admin apps. Open overlay: `ctrl+shift+alt`. |
| [openusd-live-control](https://github.com/2eezy77/openusd-live-control) | Load `tools/maya_bridge.py` in Maya; send JSON via `scripts/send_cmd.py` to `127.0.0.1:8765`. | Maya 2026 + MayaUSD, Windows. Default branch is **master**. First-run: `00_START_HERE.md`. |
| [kiad-atc](https://github.com/2eezy77/kiad-atc) | `python3 server.py` (stdlib only). Aircraft: `GET /api/aircraft`. Default **:8080**. | Needs `CESIUM_TOKEN` and `GOOGLE_KEY`. Optional `PORT` override (the README demo URL uses **8877**). Educational visualization — not an operational ATC tool. |
| [omniverse-integration](https://github.com/2eezy77/omniverse-integration) | `pip install -r 11-configuration/requirements.txt`, then inspect `01-semantic-core/core-3d-semantic-ontology.ttl` or run `python 04-tools/bidirectional-conversion-engine.py`. | Python 3.10+. `05-scripts/executive-verification.py` still looks for pre-reorg paths (`core/`, `tools/`) and is not a reliable first-run check. |

Also-shipping entry points: stem camp `python app.py` on **master** → `127.0.0.1:5000` (local demo, no auth; optional `CAMP_DB_PATH`) · parallel C `make` + Open MPI.

### Focus

- **Software systems** - sockets, Windows UIA, parallel programming (MPI / OpenMP / Pthreads)
- **Products & tooling** - Flask, React / Express-style apps, shipping end-to-end
- **Real-time / 3D** - CesiumJS, OpenUSD, Maya, Omniverse

Building and hardening full-stack products, systems tools, and 3D / geospatial pipelines.
