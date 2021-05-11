# binary files in git repo
I'm taking notes with [org-mode](https://en.wikipedia.org/wiki/Org-mode) and include pictures or link to a PDF.
These binary files are part of the git repo.
This makes the handling very simple as with the push/pull every thing is in sync without any extra steps.

But the size of the repo is now becoming a problem. Not only on the phone/tablet (_Working Copy_ on iOS) but also the notebook with a small SSD. This is not only because I checked in some large files but also as each file exists twice - the /checked out/ and the /.git/ one.

There are some readily available solution to the problem like [git-annex](https://git-annex.branchable.com/) or [git-lfs](https://github.com/git-lfs/git-lfs). But none fits exactly my requirements like
- multiple clones on the same computer should use the same binary file (my binary files are not versioned, and if there is a 2nd version, I need to link to both and point out the difference in the notes)
- the binary files need to be accessible from different repos (existing solutions require a decision in which repo to /store/ the file)

I have already a /rsync/ based workflow to sync binary data between my different computer. This could be simple advanced for this. So far I thinking at three scenarios:

- pure git repo, no binary data
- all pictures used in the notes
- all referenced binary files
