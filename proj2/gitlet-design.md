# Gitlet Design Document

**Name**:
## Designing
1. what data?
2. how to store data?
3. when to store?

## Classes and Data Structures

### Repository

#### Fields

1. staging area(add)
2. staging area(remove)
3. some commit tree
4. master pointer: points to the current commit of master branch
5. head pointer: points to the current commit of active branch
6. some blobs


### staging area(add)
#### staging an already exist file -> overwrite the older version
in .gitlet
#### how to know if a file already exists?
#### build a map: file name to current file sha1 id, and with id, find a version of
a file (blob)

#### Fields

1. 
2. Field 2

### blob
content of a file
maybe inside a folder name of its sha1 code so that it's easier to find


#### Fields

### commit
#### Fields
meta datas
2 strings represent parents
a map storing blobs





## Algorithms
### init 
a repo is never instantiated, instead a .gitlet dir is created
### Add
add a new blob
update staging area
### commit
use add and rm to update commit
rm: untrack a file in commit
1. staging area is cleared after commit
2. the commit just added become currrent commit and is added to the commit tree
### rm
* if file is staged for addition:
*  unstage
*  if file is tracked in current commit:
*      stage the file for removal and delete file in the cwd
### log
/** start from the head commit, print every commit to the initial commit.
* notice that log only prints a single line, it doesn't print the whole branch.
* when a commit has 2 or more parents, choose the first parent, and add a line about merging.
*  */
### global-log
/**Like log, but displays information about all commits.
*  The order does not matter.
*  Hint: use plainFilenamesIn in Utils to iterate over files within a directory.
* */
### branches
because user might create multiple branches, a map for branches is needed.
In order to know which branch is head, head is now a branch name, first set to "master".
(Originally head is set to a commit id)
the head always points to branch pointer(in gitlet)
add a map called branches(branch name to commit id)
## Persistence
### how to store data?



