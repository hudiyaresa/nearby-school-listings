# Nearby school listings

Interactive map of about 4,000 schools (preschool to senior high) around East Jakarta, Pondok Gede and the
western edge of Bekasi City, built to compare neighborhoods while house hunting.

**Live map:** https://hudiyaresa.github.io/nearby-school-listings/

## What it shows

- Every school in the area from the official registry: level, public or private, accreditation, students and teachers.
- Fill color is the school level (preschool yellow, primary red, junior high blue, senior high cyan, vocational
  gray, Cambridge/international purple). Public schools are solid, private schools are pale. A gold ring marks
  top public schools, a dark ring marks favorites, a pink ring marks private schools that parents talk about a lot on Threads.
- Hover or tap a school for a quick fee summary. Click it for details.
- Fees: real numbers from biayasekolah.id where available, otherwise a clearly labelled estimate range per segment.
  Public schools charge no tuition.
- Admission zones for Jakarta public schools (2026 rules): the school's RT plus touching RTs (priority 1) and the
  school's kelurahan plus neighbors. Bekasi uses straight-line distance, so a radius circle is drawn instead.
- A zone circle around the Jatiwaringin toll gate, or around any custom pin you drop (saved in your browser).
- Optional house layer pulled live from
  [house-listing-gallery](https://hudiyaresa.github.io/house-listing-gallery/). Solid green dots have an exact pin,
  hollow dashed dots are approximate (area center).
- Works on phones (filters open as a bottom sheet) and follows the system light/dark theme.

## Data sources

| Source | Used for |
|---|---|
| [datawan-labs/schools](https://github.com/datawan-labs/schools) | School list, coordinates, accreditation, size (Ministry of Education and Ministry of Religious Affairs data) |
| [biayasekolah.id](https://biayasekolah.id) | Entry fees, monthly tuition, curriculum for about 70 schools |
| Threads | Public posts and replies where parents recommend schools; counts and short quotes (in Indonesian) |
| LTMPT UTBK 2022, TKA 2026 (via news media) | Rankings of public senior and junior high schools |
| Jakarta RT boundaries (BPBD) | Admission priority polygons |
| OpenStreetMap | Base map |

## Caveats

- Senior high scores are from UTBK 2022, the last ranking LTMPT released.
- Estimated fees are not the school's own numbers. Always confirm with admissions.
- Threads mentions are counted per brand, so all campuses of the same brand share the count.
- Admission rules change every year; check spmb.jakarta.go.id and spmb.bekasikota.go.id.

The map is a single static page (`index.html` plus `data/`), with Leaflet loaded from cdnjs.
