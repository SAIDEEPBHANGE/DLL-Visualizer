# DLL Visualizer

DLL Visualizer is a static web application for exploring .NET assemblies (DLLs) and the dependencies between them. It turns scan results into an interactive view so you can see how components relate and which dependencies are local DLLs versus framework/system assemblies.

## Features

- Browse and search assemblies for SmartPlant 3D and SmartPlant P&ID
- Inspect per-DLL details: name, version, file path, runtime version and scan date
- View each assembly's dependencies and whether they are local DLLs
- Fast search powered by a background web worker

## Project structure

| Path | Description |
|------|-------------|
| `index.html` | Application entry point |
| `assets/` | Built JavaScript bundle, search worker and favicon |
| `data/SmartPlant3D/` | Product summary plus one JSON file per scanned DLL |
| `data/SmartPlantPID/` | Product summary plus one JSON file per scanned DLL |
| `data/Backend-Audits/` | Audit results from the scanning backend |

## Running locally

The app is fully static; serve the repository root with any web server:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
Dll-visualizer
