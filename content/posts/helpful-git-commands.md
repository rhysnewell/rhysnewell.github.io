+++ 
date = "2020-02-04"
title = "Git Makes Me Feel Like a Git"
slug = "helpful-git-commands" 
tags = ["Git", "Scripts", "Commands"]
categories = ["Git", "Version Control", "Tutorial"]
series = ["Informal", "Git"]
+++

### Introduction

There are many things in this world that make me truly feel like a fool.
One of them is perhaps one of the most useful tools any programmer could use: Git.
Which is unfortunate for me, considering I am a programmer... Sort of.

My understanding of how to properly use Git to its full extent is incredibly lacking. 
It's like when you "learn" another language in high school, and then when faced
with an actual real world encounter of said language you've got no idea of what is going on.

So here in this blog, I will make account of some the things I realize I don't know how to do with Git
and hopefully work out how to do them.

### Part One: Detached Heads
Okay, somehow you've lost your head. It's okay, it happens to the best of us.
We can fix this.

Step 1:

Look at the most recent commit.
```commandline
$ git log -n 1
```
Step 2:

Copy the commit hash.

Step 3:

Checkout the master branch. Don't worry about the warning that pops up, we'll handle that in step 4.

```commandline
$ git checkout master
```

Step 4:

Create a temporary branch containing your commit-hash from step 1.

```commandline
$ git branch tmp <commit-hash>
```

Step 5:

If you'd like to save the changes you made in this commit, and merge them to master then:

```commandline
$ git merge tmp
```

It's possible that doing so may cause some merge conflicts. These can be tedious to fix unfortunately,
but necessary if you want to keep your changes. Git will mark which files have conflicts
and point to them within each file using this format:

```
<<<<<<< HEAD
someone wrote this...
=======
but then someone else wrote this.
>>>>>>> branch-a

or, more likely, you wrote both of them on separate branches and forgot
you'd made the change you daft git.
``` 

Choose either the head or the branches changes, or a mixture of both. Add the file in once it
has been modified.

```
$ git add modified_file
$ git commit -m "merging conflict"
$ git push
```

That should solve your detached head. If the problem persists, see a doctor.