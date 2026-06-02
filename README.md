

# What is pgmodeler-builder

A set of Github actions for generating monthly
builds of pgModeler for both Linux, Windows, and MacOS.

## What is pgModeler?

An **open-source, multiplatform database modeler for PostgreSQL**.
This project aims to be a reference database design tool when it
comes to FOSS in the PostgreSQL ecosystem.

## What is released?

In the [releases section](https://github.com/ccamacho/pgmodeler-builder/releases)
there will be a monthly build including:

- A build tarball for MacOS, Windows and Linux compiled sources.
- An .AppImage for Linux.
- A .dmg file for ARM MacOS.
- A .exe installer for Windows.

The workflow builds two pgModeler versions each month:

- **v1.2.3** (latest stable) — built with qmake
- **v2.0.0-beta** (latest pre-release) — built with cmake

These are configured in the `matrix` sections of the
[Windows](https://github.com/ccamacho/pgmodeler-builder/blob/main/.github/workflows/builder.yml),
[Linux](https://github.com/ccamacho/pgmodeler-builder/blob/main/.github/workflows/builder.yml),
and
[MacOS](https://github.com/ccamacho/pgmodeler-builder/blob/main/.github/workflows/builder.yml)
jobs inside `builder.yml`.

For adding new versions or releases include the new ones in the
`matrix.include` list for all three platform jobs.

## What is missing?

Several optimizations could be applied to the workflow to make
the builds smaller and optimize how it runs. Any feedback and
improvements are welcomed with PRs.

- Making sure only the required libs are included.
- Avoiding duplicated builds and packages in the releases assets.
- Including commit information when creating builds from a
  branch.

## Usage hints

### Linux

- Create the default config folders: `mkdir -p ~/.config/pgmodeler-1.2`
- Make the AppImage executable: `chmod +x pgModeler-*.AppImage`

### MacOS

- Open the .dmg file and drag pgModeler to your Applications folder.

### Windows

- Run the `pgmodeler-windows-setup-*.exe` installer.

## Consider donating

If you use, like, and think pgModeler deserves 
financial contribution, go ahead and help it!.
For more details about additional features,
screenshots, and other useful information,
please, visit the [project's official website](https://pgmodeler.io).
