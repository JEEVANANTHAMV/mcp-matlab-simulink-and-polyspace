# MATLAB, Simulink & Polyspace

> Runs MATLAB scripts, Simulink models, and Polyspace code-safety checks through this assistant. Needs MATLAB installed and licensed (with Simulink and/or Polyspace if you use those features).

The bundle zip (**32.7 MB**) is stored in this repository at **`bf872169-5355-4839-b237-47c86c813bab.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `bf872169-5355-4839-b237-47c86c813bab` |
| Status in registry | active |
| Bundle size | 32.7 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `MATLAB_ROOT` | `C:\Program Files\MATLAB\R2025b` |
| `MW_MCP_SERVER_MATLAB_ROOT` | `C:\Program Files\MATLAB\R2025b` |
| `POLYSPACE_ROOT` | `C:\Program Files\MATLAB\R2025b\polyspace` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__INSTALL_DIR__\\bin\\matlab-mcp.exe",
  "args": [
    "--disable-telemetry=true",
    "--initialize-matlab-on-startup"
  ],
  "env": {
    "MW_MCP_SERVER_MATLAB_ROOT": "__MATLAB_ROOT__",
    "MATLAB_ROOT": "C:\\Program Files\\MATLAB\\R2025b"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `bf872169-5355-4839-b237-47c86c813bab.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
