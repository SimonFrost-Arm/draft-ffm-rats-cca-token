The CDDL files produced by the build and test machinery can be made into downloadable artefacts using the following procedure:

## Create a git tag

To trigger the "CDDL release" action, the tag must start with "`cddl-`".

### I-D CDDL files

When releasing the CDDL files associated with the given I-D version, use the convention:

```sh
git tag -a cddl-draft-ffm-rats-cca-token-<nn>
```

Where `<nn>` is the draft version number.

### HEAD CDDL files

When releasing the current HEAD, use:

```sh
git tag -a cddl-$(git rev-parse --short HEAD)
```

## Push the tag to origin

```sh
git push origin cddl-...
```

Pushing the tag to origin will trigger the associate GitHub action.

## Inspect the release files

If everyhing goes as planned, the 3 "autogen" CDDL files will be available for download from the following locations:

```
https://github.com/SimonFrost-Arm/draft-ffm-rats-cca-token/releases/download/cddl-.../cddl/top/top-autogen.cddl
https://github.com/SimonFrost-Arm/draft-ffm-rats-cca-token/releases/download/cddl-.../cddl/platform/platform-autogen.cddl
https://github.com/SimonFrost-Arm/draft-ffm-rats-cca-token/releases/download/cddl-.../cddl/realm/realm-autogen.cddl
```
