# Voyzu Shared Contacts Manager Help

## About

This repository hosts the online help for Voyzu Shared Contacts Manager.  If you notice an error please raise an issue in this repository's issues.

# Technical info

This help is hosted by github pages (which is built on jekyll static site genration) and uses a remote theme.  This can be seen by opening the `_config.yml` file which contains the line:
```yaml
remote_theme: mmistakes/minimal-mistakes
```

Content is written in markdown (.md files) which the jekyll engine transforms to html after any commit.  The navigation and templating engines are provided by the minimal mistakes template, which builds on standard jekyll functionality.

At build time github pages will look for the applicable page in this repository, if this is not found it will look in the minimal mistakes remote theme repository.  (this may be over-simplifying but its how it seems to work)

The following changes have been hard-coded, as the minimal mistakes theme did not seem to provide these features out of the box:

- `/assets/js/lunr/lunr-store.js` has been re-written so that content in the `_pages` directory (only) is searched

- `_includes/masthead.html` has been tweaked to delete the standard large text link in the top left of the menu.

- `_includes/footer.html` has been tweaked to remove the default link icon and to remove the copywrite line