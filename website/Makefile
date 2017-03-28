# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line.
SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = MPCS52030-OperatingSystems
SOURCEDIR     = .
BUILDDIR      = _build
DEPLOYDIR     = ../../mpcs52030-website/

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

deploy:
	cp -r $(BUILDDIR)/html/* $(DEPLOYDIR)/
	git --work-tree=$(DEPLOYDIR)/ --git-dir=$(DEPLOYDIR)/.git add -A .
	git --work-tree=$(DEPLOYDIR)/ --git-dir=$(DEPLOYDIR)/.git commit -m"Updated website"
	git --work-tree=$(DEPLOYDIR)/ --git-dir=$(DEPLOYDIR)/.git push origin gh-pages
