# Metric Ruler Builder

This project is a small website for designing simple metric rulers for 3D printing.

You enter:
- length in centimeters
- width in centimeters
- depth in centimeters
- marking precision of `0.5 cm` or `1 cm`

The site then:
- previews the ruler in the browser
- adds rounded corners and raised numbers
- shows the ruler size in millimeters for printing
- generates a direct downloadable STL file
- generates matching OpenSCAD code for editing

## Files

- `index.html` - website layout
- `styles.css` - page styling
- `app.js` - ruler logic, preview rendering, and OpenSCAD generation
- `server.js` - tiny static server for local preview

## Run Locally

You can open `index.html` directly in a browser, or run:

```bash
npm start
```

Then visit [http://localhost:3000](http://localhost:3000).

## Turn It Into a Printable Model

1. Open the website.
2. Enter the ruler length, width, and depth in centimeters.
3. Choose `0.5 cm` or `1 cm` precision.
4. Click `Download .stl` for a ready-to-slice file.
5. Or click `Download .scad` if you want an editable OpenSCAD version.
6. If you use the `.scad` file, open it in OpenSCAD and export it to STL.

## GitHub / GitHub Pages

This project is static, so it works well on GitHub Pages.

1. Create a new GitHub repo.
2. Upload the project files into the repo root.
3. Make sure at least `index.html`, `app.js`, and `styles.css` are in the repo.
4. In the GitHub repo, open `Settings` -> `Pages`.
5. Set the source to deploy from the `main` branch root.
6. Save, and GitHub Pages will publish the site.

You do not paste everything into one GitHub box. Upload the files as files in the repo.

## Notes

- The website accepts dimensions in centimeters.
- The generated OpenSCAD model uses millimeters because that is the standard unit in most 3D printing tools.
- Rounded corners are built into both the STL and OpenSCAD outputs.
- Raised numbers are added when the ruler is wide enough to keep them readable.
