

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

## Consider donating

If you use, like, and think pgModeler deserves 
financial contribution, go ahead and help it!.
For more details about additional features,
screenshots, and other useful information,
please, visit the [project's official website](https://pgmodeler.io).
