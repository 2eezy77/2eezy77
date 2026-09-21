Software engineer focused on software systems, full-stack products, and real-time / 3D tooling. Shipping production apps and pipelines; aviation visualization is one domain I apply those skills to.

**[Geoknoesis](https://github.com/2eezy77)** · **[Public work](https://github.com/2eezy77?tab=repositories)**

### Language mix

| Language | Focus |
| --- | --- |
| **Python** | Pipelines, Flask apps, OpenUSD / Maya tooling |
| **JavaScript** | React / Express products, CesiumJS viz |
| **C** | Parallel systems (MPI / OpenMP / Pthreads) |
| **SQL** | Postgres-backed product data |

### Featured builds

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/property-manager">
        <img src="https://raw.githubusercontent.com/2eezy77/property-manager/main/docs/login.jpg" alt="Montero Rentals" width="100%" />
      </a>
      <br />
      <strong>product</strong> · <b><a href="https://github.com/2eezy77/property-manager">property-manager</a></b><br />
      Live rental product ([monterorentals.com](https://www.monterorentals.com)) - tenant / manager / owner portals with Stripe ACH, Cash App, Plaid, and Postgres.
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/window-hints">
        <img src="https://raw.githubusercontent.com/2eezy77/window-hints/main/docs/overlay-google.jpg" alt="window-hints" width="100%" />
      </a>
      <br />
      <strong>systems tooling</strong> · <b><a href="https://github.com/2eezy77/window-hints">window-hints</a></b><br />
      Systems tooling for Windows - UI Automation scan, overlay codes, hotkey cursor jumps.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/openusd-live-control">
        <img src="https://raw.githubusercontent.com/2eezy77/openusd-live-control/master/docs/viewport.jpg" alt="OpenUSD Live Control" width="100%" />
      </a>
      <br />
      <strong>realtime 3D</strong> · <b><a href="https://github.com/2eezy77/openusd-live-control">openusd-live-control</a></b><br />
      Real-time 3D tooling - Maya / OpenUSD control via CLI to socket bridge to viewport.
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/2eezy77/kiad-atc">
        <img src="https://raw.githubusercontent.com/2eezy77/kiad-atc/main/docs/kiad-atc-ui.jpg" alt="Real-time aviation visualization" width="100%" />
      </a>
      <br />
      <strong>geospatial viz</strong> · <b><a href="https://github.com/2eezy77/kiad-atc">kiad-atc</a></b><br />
      Real-time geospatial viz - CesiumJS, Photorealistic 3D Tiles, live ADS-B pipeline, overlay UI.
    </td>
  </tr>
</table>

Also shipping: [omniverse-integration](https://github.com/2eezy77/omniverse-integration) · [stem-summer-camp-registration](https://github.com/2eezy77/stem-summer-camp-registration) · [csci320-parallel-programming-portfolio](https://github.com/2eezy77/csci320-parallel-programming-portfolio)

### How to run the public work

Verified against each repo's README and source. Full runbooks stay in those repos.

| Repo | Start here | Constraints |
| --- | --- | --- |
| [property-manager](https://github.com/2eezy77/property-manager) | Live: [monterorentals.com](https://www.monterorentals.com). Local: that repo's `SETUP.md`, then `npm run dev` + `client` Vite. API `PORT` defaults to **8080** (see `.env.example`). | Node 18+, Postgres. Do not rotate `ENCRYPTION_KEY` after banks are linked. Stripe webhooks need the raw body. Production webhook must include `charge.refunded` (see `docs/stripe-webhook-events.md`). |
| [window-hints](https://github.com/2eezy77/window-hints) | `python -m multiwindow_ui_hints` | Windows. Elevate with `Run-UI-Hints.ps1` for hints inside admin apps. |
| [openusd-live-control](https://github.com/2eezy77/openusd-live-control) | Load `tools/maya_bridge.py` in Maya; send JSON via `scripts/send_cmd.py` to `127.0.0.1:8765`. | Maya 2026 + MayaUSD, Windows. First-run: `00_START_HERE.md`. |
| [kiad-atc](https://github.com/2eezy77/kiad-atc) | `python3 server.py` (stdlib only). Aircraft: `GET /api/aircraft`. | Needs `CESIUM_TOKEN` and `GOOGLE_KEY`. Educational visualization — not an operational ATC tool. |

Also-shipping entry points: omniverse `05-scripts/executive-verification.py` · stem camp `python app.py` on **master** (local demo, no auth) · parallel C `make` + Open MPI.

### Focus

- **Software systems** - sockets, Windows UIA, parallel programming (MPI / OpenMP / Pthreads)
- **Products & tooling** - React, Node/Express, Flask, Postgres, Stripe ACH / Cash App, Plaid; shipping end-to-end
- **Real-time / 3D** - CesiumJS, OpenUSD, Maya, Omniverse

Building and hardening full-stack products, systems tools, and 3D / geospatial pipelines.
