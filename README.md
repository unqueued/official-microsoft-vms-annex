# official-microsoft-vms-annex

## What is this?

This is a repo that lets people track an ephemeral collection of files, using the power of git and git-annex.

We can keep an exact index of what files are made available, and automate mirroring of the files when they become unavailable from Microsoft. We can even coordinate our efforts to rebuild a file collection if files have been lost.
If you know the filenames and signitures, you can generate entries for them, which can be imported later by other users.


## Why?

It is trying to solve the problem discussed here:
https://gist.github.com/zmwangx/e728c56f428bc703c6f6
All people can do is watch, and keep track of what files are still available, and what new ones become available.

Even though I'm sure that among all the people viewing that thread, there are all of the missing files. I'm sure people would like to make them available, but there is no convenient way to do that. There is no easy way to know exactly what files are wanted, and what missing files have already been made availalbe. At best, a generous person could take time out of their day to set up a webserver and throw the files up, hoping that they have all of them. Or, the people discussing things could make a Google Drive share, but that comes with several downsides as well. How do we handle access control? And isn't it inconvenient for users to try to discern what files still need to be uploaded?

This is a test case for bigger ephemeral filesets. What if instead of dozens of ephemeral files, there were thousands? What if there were just a few files that were missing, and only a handful of users that had those missing files?

This is how it would work here. Anyone can clone this repo, copy whatever files they have into the incoming/ folder, and then do a make import, and if they have a wanted file, the index will be updated. They can then do a make mirror, which will upload it to archive.org, or some other mirroring service. Finally, they can do a pull request to inform others that they have a copy of the file.

Git is a great medium for large groups of people to systematically keep track of who has what files, and build a distributed mirror.

While this might seem like overkill, the fact that so many people are interested in this, but it hasn't been worth anyone's trouble to actually mirror anything, shows that is useful.

