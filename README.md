This knowledge base for the West Coast Ocean Data Portal was developed using Sphinx and is published at [wcodp.readthedocs.org](http://wcodp.readthedocs.org).  

Information is organized by topic and edits and contributions are welcome via GitHub.  ReadTheDocs automatically rebuilds the documentation every time a commit is made or a pull request is merged.  

Here are a few resources for reStructuredText:
* [reStructuredText Docs](http://docutils.sourceforge.net/rst.html)
* [reStructuredText Primer](http://sphinx-doc.org/rest.html)
* [Sphinx/Rest Memo](http://rest-sphinx-memo.readthedocs.org/en/latest/ReST.html)

You can also search other Read the Docs documentation to find reStructuredText syntax examples.


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
