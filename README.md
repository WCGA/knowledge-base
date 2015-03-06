This knowledge base for the West Coast Ocean Data Portal was developed using Sphinx and is published at [wcodp.readthedocs.org](http://wcodp.readthedocs.org).  

Information is organized by topic and edits and contributions are welcome via GitHub.  ReadTheDocs automatically rebuilds the documentation every time a commit is made or a pull request is merged.  

To work on this documentation on your system, checkout the code from GitHub and install Sphinx using the [RTD instructions](https://docs.readthedocs.org/en/latest/getting_started.html) for using reStructured Text.

#Command reference

```bash
cd docs
make html
```
Then open index.html in your _build directory.  

Or run autobuild service
```bash
sphinx-autobuild . _build
```