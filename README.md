# 🔶 Facet Metarepo

Facet is code-first parametric CAD in the browser: write a model in code, evaluate it with a solid-geometry kernel, preview it in 3D, and export a print-ready STL or 3MF. This metarepo groups the Facet services for local development and self-hosting.

## Services

| Service | Stack | Description |
|---------|-------|-------------|
| `facet-app` | TanStack Router / Tauri / Rust+WASM | The Studio web app and geometry kernels |

## Prerequisites

- [Bun](https://bun.sh)
- [Docker](https://docs.docker.com/get-docker) (with Compose), to run the stack in a container

## Getting Started

Facet is a single client-side app, so there is no orchestration to configure. Clone the app into `services/` and run it:

```sh
git clone https://github.com/omnidotdev/facet-app services/facet-app
cd services/facet-app
bun install
bun run dev      # https://localhost:3000
```

## Docker Compose

`compose.yaml` builds and serves the app on http://localhost:8080. Clone the app first:

```sh
git clone https://github.com/omnidotdev/facet-app services/facet-app
docker compose up --build
```

## Diagnostics

- The container serves the static SPA on `8080`; a plain `GET /` returning 200 is a sufficient liveness probe.
- Run the engine unit tests from the app: `cd services/facet-app && bun test src`.

Full documentation lives at [docs.omni.dev/products/facet](https://docs.omni.dev/products/facet).

## License

The code in this repository is licensed under Apache 2.0, &copy; [Omni LLC](https://omni.dev). See [LICENSE.md](LICENSE.md) for more information.
