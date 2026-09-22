# Facet 🔶

Code-first parametric CAD, in the browser. Write a model in code, a solid
geometry (CSG) kernel turns it into a mesh, a 3D viewport shows it live, and you
export a print-ready STL.

Live at **[facet.omni.dev](https://facet.omni.dev)**. Part of the
[Omni](https://omni.dev) ecosystem, in partnership with
[MatterForge](https://matterforge.io). Licensed under Apache-2.0.

## Repositories

Facet is a single client-side app:

- **[facet-app](https://github.com/omnidotdev/facet-app)** — the web app
  (TanStack Router + Tauri) with TypeScript and Rust/WASM geometry kernels.

## Self-hosting

Facet is a static single-page app, so any static host can serve it.

Clone and build it directly:

```sh
git clone https://github.com/omnidotdev/facet-app services/facet-app
cd services/facet-app
bun install
bun run build      # emits dist/, serve it with any static host
```

Or build and serve the container with Docker Compose (http://localhost:8080):

```sh
git clone https://github.com/omnidotdev/facet-app services/facet-app
docker compose up --build
```

See the [docs](https://omni.dev/products/facet) for details.

## License

[Apache-2.0](./LICENSE.md).
