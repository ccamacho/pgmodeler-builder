

# What is pgmodeler-builder

A set of Github actions for generating monthly
builds of pgModeler for both Linux and Windows.

## What is pgModeler?

An **open-source, multiplatform database modeler for PostgreSQL**.
This project aims to be a reference database design tool when it
comes to FOSS in the PostgreSQL ecosystem.

## What is missing?

Several optimizations could be applied to the workflow to make
the builds smaller and optimize how it runs. Any feedback and
improvements are welcomed with PRs.

- Reducing the workflow steps.
- Making sure only the required libs are included.
- Avoiding duplicated builds and packages in the releases assets.
- Deduplicating variables.
- Making releasing the versions and tags more effective, so
  far we release everytime all the labels.
- Including commit information when creating builds from a
  branch.

## What is released?

In the [releases section](https://github.com/ccamacho/pgmodeler-builder/releases)
there will be a monthly build including:

- A build tarball for the Windows and Linux compiled sources.
- An AppImage for Linux.
- A setup file for Windows.

Each release includes the tags and releases included in the
[Windows](https://github.com/ccamacho/pgmodeler-builder/blob/main/.github/workflows/builder.yml#L79)
and
[Linux](https://github.com/ccamacho/pgmodeler-builder/blob/main/.github/workflows/builder.yml#L227)
jobs at the time it was executed. Like:

```
matrix:
  branch: [ v1.1.4, 1.1.5, 1.2.0-alpha1 ]
```

For adding new versions or releases include the new ones in the list to be built.
For any new release make sure to make the update for both windows and linux jobs.

## Consider donating

If you use, like, and think pgModeler deserves 
financial contribution, go ahead and help it!.
For more details about additional features,
screenshots, and other useful information,
please, visit the [project's official website](https://pgmodeler.io).
