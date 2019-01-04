
## gvn

simplistic tool to
* generate/bump version numbers
* put tag in git
* keep module up-to-date with importable strings to display


### basic plan
* 'gvn' bumps version number string in gvn.js  (or .py...)
* commit your source (which commits version number string in gvnVersion.js or .py)
* tags previous commit with the version number string
* needs to push: `git push origin --tags`

```
  $  # various code edits; done; looks good

  $ ./gvn                                                         # bump version
  $ git commit -m "code clean; comments" -a                       # commit all files
  $ git tag -a v0.0.3 -m "small code cleanups; readme" 85da96d    # make tag on that commit
  $ git push --follow-tags                                        # push files  and tags (see config)

  $ git log --pretty="%h %d %s" --decorate=full                   # look at what you've done
```

You can then...
* display version number (and date) in your program/gui
* find the version number tag in git: `git tag`
* see your working commit and #-commits since last tag:  `git describe`
* compact show logs: `git log --pretty="%h %d %s" --decorate=full`


### other things
* --follow-tags   or `git config --global push.followTags true` 
* could use `git notes` - add notes to commit? to tag?

### various non-answers
* https://stackoverflow.com/questions/37814286/how-to-manage-the-version-number-in-git
* https://git-scm.com/book/en/v2/Git-Basics-Tagging

