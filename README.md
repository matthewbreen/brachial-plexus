# Brachial Plexus Neurogram Playground

A browser-based teaching sandbox for reading the brachial plexus on sagittal MRI. It was built from Matt B's segmentations and his talk on plexus anatomy.

It runs entirely in the browser as plain static files, with no build step and no server code.

## Cases

| Case | What it is |
| --- | --- |
| Ideal plexus | An idealized normal-calibre plexus on a stylized, artifact-free MRI |
| Thickened plexus | Matt B's Visage segmentation of a thickened plexus (3D STIR SPACE post-contrast) |
| Normal · left (reference unilateral) · Case B | The reference normal unilateral case |
| Normal · bilateral | A normal bilateral exam (3D STIR SPACE) |
| CT neck with contrast · unsegmented | No labels: find each level yourself |

## Modes

- **Explore**: 3D surfaces with MIP, linked sagittal, coronal and axial slices, a structure legend and a plexus diagram.
- **Sagittal walk**: steps through roots → trunks → divisions → cords → branches.
- **Quiz**: name a highlighted structure.

The layout switches to a one-view-at-a-time phone version on small screens.

## Publishing on GitHub Pages

1. Push this folder to the root of a repository.
2. Go to **Settings → Pages**.
3. Choose **Deploy from a branch**, then select `main` and `/ (root)`.

The included `.nojekyll` file makes Pages serve the files as they are.

To try it locally, run `python3 -m http.server` in this folder and open http://localhost:8000. Opening `index.html` directly from disk won't work, because browsers block local data fetches.

## Notes

- Edits, notes and seed ROIs made in this copy are saved only in the viewer's own browser (localStorage).
- Image volumes are de-identified 1 mm resamples stored as PNG mosaics. They contain no DICOM headers.
