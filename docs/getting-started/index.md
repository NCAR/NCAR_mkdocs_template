# How to Use this Template Repository? 🛠️

**Estimated time to completion: 20 minutes**

In this page, you will find information on how to start your own docs project using this template. This guide will walk you through the steps of getting started with such a template, including initial setup, customization, and deployment.

## Step1: Create a New Repository Using This Template

1. Open this repository Github page: [https://github.com/NCAR/NCAR_mkdocs_template](https://github.com/NCAR/NCAR_mkdocs_template) and click the **"Use this template"** button on the top right of [this repository](https://github.com/NCAR/NCAR_mkdocs_template) to create a new repository using this template. Please see the image below for reference:


![Use this template](./assets/use-this-template.png)


2. One you click on "Use this Template" and "Create a new repository", Github opens a new page. Here give your repository a name. Then click "Create Repository". This will create a new repository under your account with the same files and structure as this repository.

In general, the reposiotry is organized into the following sections:

```
mkdocs.yml        # The MkDocs configuration file.
themes/           # Customized theme files.
    ...           # (sourced from https://github.com/NCAR/NCAR_mkdocs_material_themes)
docs/
    index.md      # The documentation homepage.
    ...           # Other markdown pages, images and other docs files.
conda.yaml        # A conda environment definition with the Python dependencies to build the project.
.readthedocs.yml  # The configuration file for readthedocs hosting.
```

## Step 2: Modify your Repository to include your content:

Once the repository is created, you can clone it to your local machine and start working on it. You can add new markdown files, images, and other documentation files to the `docs` directory. You can also customize the `mkdocs.yml` file to change the site name, navigation, and other settings.



First, edit the `mkdocs.yml` file to customize the site name, navigation, and other settings. For example, you can change site name, site description, and author:

```
# ------------------------------------
# -------- Project Information -------
# ------------------------------------
site_name: NCAR MkDocs Template
site_description: A template for creating NCAR mkdocs
repo_url: https://github.com/NCAR/NCAR_mkdocs_template/
site_url: https://NCAR.github.io/NCAR_mkdocs_template/
site_author: CISL CSG (Consulting Services Group)
```

You can also customize the navigation by editing the `nav` section of the `mkdocs.yml` file. For example, you can add new pages to the navigation:

```
# ------------------------------------
# -------- Navigation ----------------
# ------------------------------------
nav:
  - Home: index.md
  - Example Page 1:
	- Example Subpage 1: example-page-1/example-subpage-1.md
	- Example Subpage 2: example-page-1/example-subpage-2.md


  - Contributing: contributing.md
  - About:
	- License: about/license.md
	- Release Notes: about/release-notes.md
```

Please see the [MkDocs documentation](https://www.mkdocs.org/user-guide/configuration/) for more information on customizing the `mkdocs.yml` navigation and other settings.

## Step 3: Building the Documentation Locally

### Building the Documentation Locally

If you want to build the documentation locally to see the changes you've made, you can do so by following these steps:

#### Create a `conda` Environment
To build the documentation locally and preview it, you'll need to install certain dependencies. Although this step is optional, we strongly recommend it.

The example provided here creates a new  `conda` environment named `mkdocs` from the provided `conda.yaml` file.

  ```bash
  conda env create -f conda.yaml
  conda activate mkdocs
  ```
##### Preview Documentation Locally
You can preview your documentation locally to make sure that your changes do not introduce any errors. With MkDocs, you can preview your changes by running `mkdocs serve` in your terminal. This starts a local server where you can preview your work.

  ```
  mkdocs serve --strict
  ```

!!! note
      `--strict` flag will enable strict mode and treat warnings as errors. This is useful to ensure that your changes do not introduce any issues such as new pages that does not exist.  Occasionally you may want to omit the `--strict` flag, for example when adding new pages that have not yet been committed through `git`.


Please note that while building and previewing the documentation locally, is optional, it is a good practice to do so to ensure that your changes do not introduce any errors.

## Step 4: Deploying the Documentation

Once you have made your changes and are ready to deploy the documentation, you can do so by following these steps:

1.Go to [ReadTheDocs.org](https://readthedocs.org/) and sign in with your Github account.

2. Click on "Import a Project" and select this new repository from the list of your repositories.

3. Once the repository is imported, ReadTheDocs will automatically build the documentation and host it at a unique URL. You can access the documentation at this URL and share it with others.




## New User Resources
* [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)
* [mkdocs documentation](https://www.mkdocs.org/user-guide/configuration/)
* [Material for MkDocs documentation](https://squidfunk.github.io/mkdocs-material/)
* [ReadTheDocs documentation](https://docs.readthedocs.io/en/stable/)
* [NCAR HPC Documentation](https://ncar-hpc-docs.readthedocs.io/en/latest/)
