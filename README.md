# yt-dlp for Vista+

[![build](https://github.com/3dyd/yt-dlp-builds/actions/workflows/build.yml/badge.svg)](https://github.com/3dyd/yt-dlp-builds/actions/workflows/build.yml)

This repository automatically builds `yt-dlp_x86.exe` (32-bit, so it works on both 32- and 64-bit systems) with **Windows Vista** as the minimum supported Windows version (official yt-dlp requires at least Windows 8).

To do that it uses Vista-compatible Python ([3dyd/cpython#v3.12.11-vista](https://github.com/3dyd/cpython/releases/tag/v3.12.11-vista)) and PyInstaller ([3dyd/pyinstaller-builds](https://github.com/3dyd/pyinstaller-builds)).

Releases in this repository are built from the same tags as [official releases](https://github.com/yt-dlp/yt-dlp/releases/).

## Update

Read the [UPDATE topic](https://github.com/yt-dlp/yt-dlp/?tab=readme-ov-file#update) in the official yt-dlp documentation for the background.

These custom yt-dlp binaries have `stable` channel (tracks this repository) and `nightly` channel (tracks [3dyd/yt-dlp-nightly-builds](https://github.com/3dyd/yt-dlp-nightly-builds)). So `--update` and `--update-to stable|nightly` commands work and update to these custom binaries.

If you want to switch from different repository, `--update-to` accepts also repository name. Example: `--update-to 3dyd/yt-dlp-builds`.

## How to Build

To make your own build, fork this repository and go to `Actions` → `build` → `Run workflow`.

Specify required inputs and either uncheck `Rebuild PyInstaller` or also fork [3dyd/pyinstaller-builds](https://github.com/3dyd/pyinstaller-builds) and specify forked repository in corresponding inputs. In the latter case you would also need to set up PAT in your `yt-dlp-builds` fork so it can trigger workflow in `pyinstaller-builds` fork.
