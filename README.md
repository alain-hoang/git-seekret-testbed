# git-seekret test repository

This test repository some random found keys around the Internet in different
files, mostly from Github.

This couldn't have been made possible without the great contributions of people
committing private and sensitive keys to Github. Many thanks to the projects
involved:

- https://github.com/bassparadize/bassparadize
- https://github.com/whodini/whodini-web-site
- https://github.com/snappler-hub/puntos

## No shame, just be considerate

The list above is not meant to be shame list of ~~old~~ projects that contain
credentials. But it's important to consider preventing this sort of stuff in the
first place.

Read more on committing credentials: http://www.itnews.com.au/news/aws-urges-developers-to-scrub-github-of-secret-keys-375785

## Using this repository

In order to properly test this repository, you will need to install
`git-seekret` with the script found in the 18F/laptop repository. At the time of
this writing, the `seekret` branch is what you should be using to install the
script. In the future, the `master` branch will be used.

```
BRANCH=seekret curl -s "https://raw.githubusercontent.com/18F/laptop/$BRANCH/seekrets-install" | sh -
```
