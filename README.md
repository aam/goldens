A repository for golden image files that are used by tests in https://github.com/flutter/flutter.

See: https://github.com/flutter/flutter/wiki/Writing-a-golden-file-test-for-package%3Aflutter

PLEASE READ THAT WIKI PAGE BEFORE CONTRIBUTING TO THIS REPOSITORY.

IT CONTAINS RULES THAT YOU MUST FOLLOW.

## Getting diffs for golden images

If you have ImageMagick and you want to use it to show diffs of files
in this repo, add the following to your `~/.gitconfig`:

```
[diff "image"]
    command = /path/to/this/repo/diff-images.sh
```

## Obsolete files

To make it easier to land multiple PRs that change the goldens in
parallel, when we change the result of a test, rather than just
updating the golden file, we change the name of the golden file
used in the test, so that after the change we use a different
image than before the change.

This section lists the files that can now be deleted because
they have been replaced in this way:

- packages/flutter/test/material/floating_action_button_test.clip.1.png
