# SecTools

**What is this?**

These are a bunch of tools that I use, in Docker images. Most of them are related to security testing.

## Sourcegraph

If you need to import a project that is not under git, you can do the following:

1) If the source code isn't a Git repository, init one
2) Create a corresponding repository in `/repos`: `git init --bare`
3) Create a remote to `/repos` and push into it
4) In the container, start the git deamon: `git daemon --reuseaddr --export-all --base-path=/repos /repos` (you may need to `apk add git-daemon` before)
