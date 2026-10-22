<p align="center"><img src="https://raw.githubusercontent.com/go-sciio/brand/main/social/go-sciio.png" alt="go-sciio" width="720"></p>

# go-sciio

🌐 **[Website](https://go-sciio.github.io)** · 📚 **[Documentation](https://go-sciio.github.io/docs/)**

**Scientific file formats in pure Go (CGO=0): HDF5, MAT, NetCDF, FITS, npy, Matrix Market, WAV and FLAC. Planned, wave 2: no library exists yet.**

go-sciio is the organisation the [go-scikit parity plan](https://github.com/go-scikit/roadmap/blob/main/PLAN.md)
names for what MATLAB's file functions and Mathematica's `Import` read and
write. Nothing is released and no code is written: this page, the website and
the documentation say what the organisation will cover and how each part will be
checked. The state of every item is in
[STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md).

## What it will cover

| Planned package | Format | Validated against |
|-----------------|--------|-------------------|
| `h5` | HDF5 (File Format Specification 3.0), reader and writer | h5py, `h5dump`, the HDF Group's example files |
| `mat` | MAT-files v4, v5, v7 and v7.3 (on `h5`) | `scipy.io`, h5py for v7.3 |
| `netcdf` | NetCDF classic (CDF-1, 2, 5) and NetCDF-4 (on `h5`) | netcdf-c `ncdump`, the netcdf-c test files |
| `fits` | FITS 4.0: images, binary tables, compressed images | astropy.io.fits, NASA's FITS samples |
| `npy` | NumPy `.npy` and `.npz` | NumPy |
| `mtx` | Matrix Market, coordinate and array | `scipy.io.mmread` |
| `wav` | WAV (PCM and float) | `scipy.io.wavfile` |
| `flac` | FLAC (RFC 9639), decoding | the FLAC test files of the IETF working group |

The package names are provisional. The plan places go-sciio in wave 2 (item 9):
HDF5 first, then MAT v7.3 on it, then NetCDF, FITS and npy. Whether `h5` wraps an
audited existing package or is written here is still open in the roadmap's
bibliography. go-sparse's wave 1 already lists Matrix Market I/O, so the line
between its work and `mtx` is yet to be drawn.

## Repositories

| Repo | What it is |
|------|------------|
| [**docs**](https://github.com/go-sciio/docs) | the documentation site (Hugo + Hextra), served at [/docs/](https://go-sciio.github.io/docs/) |
| [**go-sciio.github.io**](https://github.com/go-sciio/go-sciio.github.io) | the landing page (Hugo) |
| [**brand**](https://github.com/go-sciio/brand) | logo, icons and social images |

No library repository exists yet: each is created when its first pull request is ready.
