<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. Replaces upstream GridCraft's README. -->
<p align="center">
  <img src="assets/app-icon/freeandiy-sheets-1024.png" width="128" alt="FreeANDIY Sheets icon">
</p>

<h1 align="center">FreeANDIY Sheets</h1>

<p align="center">
  <b>A free, open-source spreadsheet. Native Rust, runs on macOS, Windows, Linux and in the browser.</b><br>
  Part of <a href="https://freeandiy.freeandy.agency">FreeANDIY</a>, free creative and office apps by Free Andy Agency.
</p>

---

## About

FreeANDIY Sheets is a spreadsheet with a ribbon interface: formulas and functions, tables,
charts, pivot tables, conditional formatting, data validation, and XLSX, CSV, HTML and PDF import
and export. It is a native egui app (no webview), and the web version is the same Rust code
compiled to WebAssembly.

Every action is a command, so the app can be driven from a CLI (`freeandiy-sheets-cli`), a JSON
control channel or an MCP server.

**FreeANDIY Sheets is based on the open-source project
[GridCraft](https://github.com/storytold/gridcraft) (© ArtCraft Team and contributors,
MIT/Apache-2.0). FreeANDIY is not affiliated with the ArtCraft team.** The editor itself is their
work; FreeANDIY adds its own branding, packaging and translations, and follows upstream closely.

## Download

Builds for macOS, Windows and Linux are published on the
[Releases](https://github.com/FreeAndy21/freeandiy-sheets/releases) page as
`freeandiy-sheets-<version>-<os>-<arch>.*`.

## Build from source

Requires Rust (see `rust-version` in `Cargo.toml`).

```sh
cargo run --release -p gridcraft                         # desktop app (binary: freeandiy-sheets)
cargo run --release -p gridcraft-cli -- --help           # CLI (binary: freeandiy-sheets-cli)
cd apps/gridcraft-web && trunk build --release           # web build (WebAssembly)
```

The crate names keep upstream's `gridcraft-*`, so upstream changes merge cleanly. The developer documentation in `docs/` is
upstream's and still says GridCraft.

## How this fork is made

Everything FreeANDIY changes lives in [`freeandiy/`](freeandiy/): the brand definition
(`branding.toml`, `app.toml`), assets, a handful of small patches and text rules. All other files
are regenerated from upstream GridCraft by `freeandiy/scripts/regenerate.sh`, so updates from
upstream never conflict. See [`freeandiy/docs/upstream-sync.md`](freeandiy/docs/upstream-sync.md).

Issues with FreeANDIY builds go to
[our tracker](https://github.com/FreeAndy21/freeandiy-sheets/issues), not to upstream.

## License

The code is licensed, like upstream, under either of [MIT](LICENSE-MIT) or
[Apache-2.0](LICENSE-APACHE) at your option. See [`NOTICE`](NOTICE) and [`ATTRIBUTION.md`](ATTRIBUTION.md)
for third-party material.

The FreeANDIY and Free Andy Agency names, the angel Andy, logos and app icons are © Free Andy
Agency and **not** covered by the code license; see
[`freeandiy/assets/brand/LICENSE-brand.txt`](freeandiy/assets/brand/LICENSE-brand.txt).

<sub>Microsoft and Excel are trademarks or registered trademarks of Microsoft Corporation in the United
States and/or other countries. FreeANDIY Sheets is an independent, open-source project and is not
affiliated with, sponsored by or endorsed by Microsoft Corporation; these names are used only to describe the
workflows it is compatible with.</sub>
