# Local preview

Trip reports are edited in `trips/*.md`. Their styling lives in `_layouts/trip.html`.

For a plain static server, install the preview dependencies once:

```powershell
python -m pip install --target .preview-packages -r requirements-preview.txt
```

After editing a report, rebuild its generated HTML:

```powershell
python scripts/build-trips.py
```

Serve the project folder, if a server is not already running:

```powershell
python -m http.server 8000
```

Open http://localhost:8000/trips/2024-03-peru.html and refresh after rebuilding.

Jekyll uses the Markdown and layout directly. `_config.yml` excludes the generated
Peru HTML from Jekyll's inputs so that it does not conflict with the Markdown permalink.

