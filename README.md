# CSI website

The CSI website is built using the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
You just need to work on markdown files and MKdocs will render them to proper web pages.


## Setup


1. Create a python virtual environment and activate it

```bash
conda create -n csi python=3.13
conda activate csi
```

2. Install the required packages
```bash
pip install -r requirements.txt
```

3. Clone the repo

```
git clone https://github.com/X-lab-3D/csi/

cd csi
```

4. Monitor local changes

```bash
mkdocs serve -w docs -w mkdocs.yml
```

then you can open http://127.0.0.1:8000/ in your browser to view the website.

## Add a new page

For example, we want to add a new page with title "Posters". You can follow these steps:

1. Add a new markdown file in the `docs` directory, e.g., `docs/posters.md`.
2. Update `mkdocs.yml` to add the new page under the `nav` section:

```yaml
nav:
- About: index.md
- Schedule: schedule.md
- Posters: posters.md
```

3. Then you can go to http://127.0.0.1:8000/posters/ to check the new page.

4. Add new content to the `docs/posters.md` file with markdown format. To make the content fancier, you can check the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Publish the changes

Once you are satisfied with your changes, you can publish them by following these steps:

Push the changes to github pages
```bash
mike deploy -p -u 2025 latest
```
