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

```shell
BRANCH=seekret curl -s "https://raw.githubusercontent.com/18F/laptop/$BRANCH/seekrets-install" | sh -
```

Once you've installed `git-seekret` in your path. You should be able to confirm
that all the rules are enabled.

```shell
git seekret rules
```

Once you've verified `git-seekret` and the rules are all where and how they
should be, you can copy the contents of any of the `*.example.yml` files to
create new commits. Once you've created new lines with new secrets to test you
can add the files to your stage and then proceed to commit your changes using
`git commit`. To check for secrets without committing, you can also run the
following command once you've staged file changes.

```shell
git seekret check -s
```

### Contributing examples which match rules

Because `git-seekret` will prevent you from committing examples which match the
secret rules, you will need to bypass the pre-commit hook in order to add your
changes to this repository.

```shell
git commit --no-verify
```
