---
title: Merging Projects
description: "Merging riverscapes projects together"
banner: true
isHome: false
---

The merge tool is an experimental tool that allows you to merge multiple Riverscapes projects together. This is useful when you have multiple projects that cover an area of interest and you want to combine them into a single project. 

The merge tool can only merge projects of the same type. For example, you can merge multiple RSContext projects together, but you cannot merge an RSContext project with a VBET project.

Currently, the merge tool only operates on rasters and GeoPackage layers. It does not operate on ShapeFiles, SQLite databases, reports, logs or other project contents!

Note that the output merged project is of the same type as all the input projects. Once uploaded into the Data Exchange, the merged project will be available for download and use in the same way as any other project, including any of the [Viewer](https://viewer.riverscapes.net) softwares.

# Considerations

The merge process downloads each individual project from the Data Exchange, merges them together. You need sufficient disk space on the code space to store all the projects that you are merging together, as well as the merged output. Big project types, such as tauDEM, might need a large code space. 

# Preparation

Create a collection within the Riverscapes Data Exchange and add all the projects that you want to merge together.

You can add projects of different types (e.g. RSContext and VBET), but when it comes to merging you will only be able to merge together projects of the same type. In other words, you can add all the projects any type for your area of interest to the collection. Then run the merge tool multiple times, once for each type of project.

Note down the collection GUID. The easiest way to do this is to open the collection in the Data Exchange and copy the GUID from the URL. The URL will look something like this:

```
https://data.riverscapes.net/c/fc198d51-c154-497e-9972-38929a047544/
```

You just want the GUID that comes after the `/c/` in the URL. Remove the trailing `/` if it is there.

# Merging Projects

1. Open a CodeSpace in the [Riverscapes Tools](https://github.com/Riverscapes/riverscapes-tools) GitHub repository.
1. Make sure you are using the `CYBERCASTOR.code-workspace`. This is not opened by default when you start the code space.
1. Open the `launch.json` file in the `.vscode` folder and find the configuration entry for `EXPERIMENTAL Merge Projects`.
  1. Enter the project type machine code. The easiest way to find this is to search the Data Exchange for the project type and look at the URL that will contain the project type string as one of the query parameters.
  1. Put the collection GUID to the `args` array, replacing the one that's there already.
  1. Provide a name for the merged project.
1. Save the `launch.json` file.
1. Run the `EXPERIMENTAL Merge Projects` configuration using the debug play menu. The merged project will be placed at the location specified in the last launch.json configuration parameter. This output folder is created under `/workspaces` (I think).

# Upload to Data Exchange

Once you have merged the projects, you can upload the merged project to the Data Exchange. You can do this using the [rscli](https://developer.riverscapes.net/dev-tools/rscli/) command line interface. Be sure to use the correct owning organization.

**WARNING**: Onced the merged project is uploaded, it's tempting to add it to the same collection as the input projects (after all, it's the same area of interest). However, this will cause the merge tool to try to merge the merged project with the input projects should you need to re-run the merge tool! It's better to create a new collection for the merged project(s).