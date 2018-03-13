# iiif-server-custom
Repository for tracking the GU customizations made to the Loris IIIF server code.

**Note: Loris is an implementation of the IIIF Image API 2.0 available at the following GitHub repo: https://github.com/loris-imageserver/loris. This repository is for tracking the Georgetown University customizations made to release v2.1.0 of the Loris source code.**

## Customizations
#### Resolver
The loris/resolver.py file has been updated with a custom SlashSubFSResolver that has the following features:
* **slash substitute** - Allows the slash_sub setting in the config file to specify a substitute string for the directory separator so that encoded slashes don't need to be used
* **directory traversal check** - Checks for attempts at directory traversal in the provided identifier, returning an "image not found" error and logging a warning if detected
