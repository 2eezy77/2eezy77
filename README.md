Software engineer focused on software systems, full-stack products, and real-time / 3D tooling. Shipping production apps and pipelines; aviation visualization is one domain I apply those skills to.

**[Geoknoesis](https://github.com/2eezy77)** · **[Public work](https://github.com/2eezy77?tab=repositories)**

### Language mix

| Language | Focus |
| --- | --- |
| **Python** | Pipelines, Flask apps, OpenUSD / Maya tooling |
| **JavaScript** | CesiumJS viz (inline HTML client; no TypeScript in public repos) |
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

Verified against each repo's README and source (2026-11-02). Full runbooks stay in those repos. No public application source has changed since 2026-07-21.

| Repo | Start here | Constraints |
| --- | --- | --- |
| [window-hints](https://github.com/2eezy77/window-hints) | `python -m pip install -r requirements.txt`, then `python -m multiwindow_ui_hints` | Windows. Elevate with `Run-UI-Hints.ps1` (UAC) for hints inside admin apps. Open overlay: `ctrl+shift+alt` (`HOTKEY_OPEN`). Optional `.exe`: `build-exe.ps1`. |
| [openusd-live-control](https://github.com/2eezy77/openusd-live-control) | `scripts\run_maya.bat`, load `tools/maya_bridge.py` in Maya Script Editor (**Python** tab), then `scripts\send_cmd.py` → `127.0.0.1:8765`. | Maya 2026 + MayaUSD, Windows. Default branch is **master**. First-run: `00_START_HERE.md`. |
| [kiad-atc](https://github.com/2eezy77/kiad-atc) | `python3 server.py` (stdlib only). Aircraft: `GET /api/aircraft` (adsb.lol → OpenSky). Binds **127.0.0.1**, default **PORT=8080**. | Needs `CESIUM_TOKEN` and `GOOGLE_KEY` (injected into `index.html` at request time). Optional `PORT` (README demo uses **8877** and `/?portfolio=1`). Educational visualization — not operational ATC. |
| [omniverse-integration](https://github.com/2eezy77/omniverse-integration) | `pip install -r 11-configuration/requirements.txt`, then inspect `01-semantic-core/core-3d-semantic-ontology.ttl` or run `python 04-tools/bidirectional-conversion-engine.py`. | Python 3.10+. `05-scripts/executive-verification.py` still looks for pre-reorg paths (`core/`, `tools/`) and is not a reliable first-run check. |
| [stem-summer-camp-registration](https://github.com/2eezy77/stem-summer-camp-registration) | `pip install -r requirements.txt`, then `python app.py` → `127.0.0.1:5000`. Tests: `python -m pytest tests -q`. | Default branch **master**. Local demo only: no auth on `/`, `/register`, or `POST /staff/cancel/<id>`. Optional `CAMP_DB_PATH` (default `camp.sqlite3`). |
| [csci320-parallel-programming-portfolio](https://github.com/2eezy77/csci320-parallel-programming-portfolio) | `sudo apt install -y build-essential openmpi-bin libopenmpi-dev`, then `cd week02-mpi-summation && make && mpirun -np 4 ./sum_static 10000000`. | C11 (`-std=c11`), not C++. Needs GCC + Open MPI. Same histogram / Monte Carlo problem is implemented three ways (MPI, Pthreads, OpenMP). |

### Common pitfalls

- **window-hints** — a second process binds `127.0.0.1:58471` and exits **2** if the app is already running. Quit from the tray, or set `UI_HINTS_ALLOW_MULTI=1` to skip the lock. There is no control window; interact via overlay, hotkeys, and the tray.
- **openusd-live-control** — `Connection refused` means the Maya bridge is not loaded. Use the Script Editor **Python** tab (not MEL), then `exec(open(r'...\tools\maya_bridge.py').read())`. Success log: `Listening on 127.0.0.1:8765`.
- **kiad-atc** — `server.py` always binds **127.0.0.1**, so the `Procfile` / `runtime.txt` (python-3.11) deploy path will not accept platform traffic. The server warns if either map key is shorter than 20 characters. Aircraft cache TTL is 8s; the client polls `/api/aircraft` every 5s.
- **omniverse-integration** — the root README's "verify" step (`executive-verification.py`) checks the old layout (`core/3d-semantic-core.ttl`, `tools/*.py`). Use the numbered folders after the reorg.
- **stem-summer-camp-registration** — Flask `debug=True` and a default `FLASK_SECRET_KEY`. Email text is queued in SQLite; SMTP is not wired.

### Focus

- **Software systems** - sockets, Windows UIA, parallel programming (MPI / OpenMP / Pthreads)
- **Products & tooling** - Flask apps, shipping end-to-end
- **Real-time / 3D** - CesiumJS, OpenUSD, Maya, Omniverse

Building and hardening full-stack products, systems tools, and 3D / geospatial pipelines.
