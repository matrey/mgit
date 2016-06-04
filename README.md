# mgit
For versioning just 1 file (or a handful), in the middle of a non-empty folder and/or several other repos

### How it works

This wrapper acts on GIT_DIR to force git to use a custom folder (.mgit.<project code>), therefore allowing several projects to coexist in the same path.

The clone function is also reworked, so that it:
* does not complain about the working directory being non-empty
* brings in the working directory the first level files from the repo, that are not hidden, and whose name (without extension) is not all uppercase
* skips files that already exist in the working directory (no overwrite)

### Usage

```
mgit <project code> ... rest of git command ...
mgit <project code> clone <repo URL> [path to deploy key]
```
