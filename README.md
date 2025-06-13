# GIG Cymru NHS Wales - {Documentation Site Title}

> ## How to use this template
>
> ### 1. Create a new repository based on this template
>
> See [GitHub Creating a Repository from a Template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).
>
> ### 2. Replace all references to `documentation-site-template`
>
> Replace this with the name of your new repository derived from this template.
>
> Specifically will need to update the following files:
>
> ```sh
> Makefile
> mkdocs.yml
> pyproject.toml
> README.md
> ```
>
> ### 3. Setup GitHub Pages
>
> In the Settings for your repository in GitHub.com under the **Pages**
section, ensure the `source` is set to **Deploy from a branch** and select
`gh_pages` as the branch.
>

---

[![mkdocs](https://github.com/GIG-Cymru-NHS-Wales/documentation-site-template/actions/workflows/publish.yml/badge.svg)](https://github.com/GIG-Cymru-NHS-Wales/documentation-site-template/actions/workflows/publish.yml)

The documents in this repository are published to [https://gig-cymru-nhs-wales.github.io/documentation-site-template/](https://gig-cymru-nhs-wales.github.io/documentation-site-template/).

## Getting Started

There are several ways to set up your development environment:

### 1. GitHub Codespaces (Recommended)

The fastest way to start contributing:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/GIG-Cymru-NHS-Wales/documentation-site-template?quickstart=1)

This provides:

* A pre-configured VS Code environment (with useful extensions installed)
* All required dependencies installed
* Automatic port forwarding for preview
* Git integration

Once you have successfully launched Codespaces you can run the
development server from the VS Code Terminal:

```bash
    make run
```

You will be prompted to **Open in Browser** to view the locally running site.

See the [Quickstart Guide](http://docs.github.com/en/codespaces/quickstart) for
more information.

Note: It can take a few minutes to fully launch Codespaces the first time, but
is faster on subsequent launches as the environment is then cached.

### 2. Local Development

**Prerequisites:**

* Python 3.11 or higher
* [uv](https://github.com/astral-sh/uv) for package/env management
* Git

**Setup Steps:**

Clone the repository:

```bash
    git clone https://github.com/GIG-Cymru-NHS-Wales/documentation-site-template.git
    cd documentation-site-template
```

Install uv (if not already installed):

```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
```

Set up environment and dependencies:

```bash
    uv sync
```

Start the development server:

```bash
    uv run mkdocs serve
```

View the documentation at: ``http://127.0.0.1:8000/``

### 3. Container-based Development

If you prefer using containers:

**Prerequisites:**

* [Podman](https://podman.io/) or [Docker](https://www.docker.com/)

**Setup Steps:**

Build the container:

```bash
    podman build --tag mkdocs .
```

Run the development server:

```bash
    podman run -p 8000:8000 mkdocs
```

View the documentation at: ``http://127.0.0.1:8000/``

### 4. Make-based Workflow

For those familiar with Make:

```bash
    # See available commands
    make help

    # Full build and serve
    make
```

View the documentation at: ``http://127.0.0.1:8000/``

## Documentation

Our documentation is built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Contributing

1. Choose your preferred development environment from above
2. Create a new branch for your changes
3. Make your changes
4. Test your changes locally
5. Submit a Pull Request

## License

This repository is licensed under the [MIT License](LICENSE)
