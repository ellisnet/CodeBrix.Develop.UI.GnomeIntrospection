# CodeBrix.Develop.UI.GnomeIntrospection

A snapshot repository of GObject Introspection (GIR) XML files, consumed by the
`CodeBrix.Develop.UI.BindingTool` code generator when producing the C# bindings
in the [CodeBrix.Develop.UI](https://github.com/ellisnet/CodeBrix.Develop.UI)
repository.

This repository contains **data files only** — no source code and no build. The
`.gir` files are machine-generated API descriptions of GNOME-platform libraries
(GTK 4, GtkSourceView, GLib, GObject, Gio, Pango, libadwaita, GStreamer,
WebKitGTK, and friends), produced by each library's own build via GObject
Introspection's `g-ir-scanner`.

## Layout

| Item | Contents |
|---|---|
| `linux/` | All 31 `.gir` files of the upstream snapshot, Linux variants |
| `macos/` | The 25 macOS variants |
| `windows/` | The 26 Windows variants |
| `gir_files.txt` | Upstream manifest: cross-platform gir files with source package + version |
| `gir_files_linux.txt` | Upstream manifest: Linux-only extras (GdkX11, GdkWayland, WebKit, ...) |
| `gir_files_windows.txt` | Upstream manifest: Windows-only extras (GdkWin32) |

This is the **complete** set of `.gir` files shipped by the upstream snapshot —
not just the ones CodeBrix.Develop.UI currently generates bindings from — so
future bindings (GStreamer, WebKit, libadwaita, ...) need no further hunting
for introspection data.

## License and Provenance

This repository is licensed under the GNU Lesser General Public License,
Version 2.1 (see the `LICENSE` file) — the same license used by the upstream
gir-files repository, and the license of the majority of the libraries whose
introspection data is included here. Some individual files describe libraries
that use other licenses (MIT, BSD-style, or dual licenses);
`THIRD-PARTY-NOTICES.txt` records the license of each.

See `THIRD-PARTY-NOTICES.txt` for full provenance and per-library
license details.
