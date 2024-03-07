# Cooperative Git

## The Mission

As you surely know Git is a powerful versioning tool, what you might not know however is that it's also a top tier **collaborative** one. As a project is rarely carried out alone this challenge will have you work in teams using Git and Github, plus a bit of [MarkDown](https://en.wikipedia.org/wiki/Markdown), in a little game of [exquisite corpse](https://en.wikipedia.org/wiki/Exquisite_corpse). Get into groups and follow the instructions below to get started, beware the dreaded "_[merging conflict](https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts)_"!

### 1. Initialization (_solo_)

- fork the repository on your Github account
- initialize a file called _poem.md_ at it's root
- give a title to your story
- clone the repository
- create a _development_ branch
- go to that branch
- write 3 lines of text to begin the story (_use some [MarkDown](https://www.markdownguide.org/basic-syntax/)_)
- commit/push the changes to the branch _development_
- invite the other members of the group as contributors

### 2. Contributions

- check a repository where you have been invited
- clone said repository
- list the existing branches
- go to the branch _development_
- create a branch called _your-name_ from there
- write 3 lines of text in the `poem.md` file to begin the story (_use some MarkDown_)
- commit the changes to the branch _your-name_
- merge your branch with _development_
- push the branch _development_
- do this for all members of the group

### 3. Versioning

- go back to your repository when all your colleagues are done
- merge _development_ with the branch _main_
- make a tag of _main_ called _version-1_

### 4. Correction

- create a new branch _corrections_ from _main_
- correct all misspellings (_if there are none add the mention perfect_)
- commit/push
- merge with _main_
- delete all the branches except _main_

### 5. Wrapping Up

If, by chance, you did not encounter any _merging conflicts_ during the exercise (_which would be downright voodoo_). You should still make sure to understand how to deal with them correctly. **You will face them** during your carreer, therefore **you need to know how to solve them**.

> **NOTE**: Make sure everyone in your group feels confortable with the challenge before calling it done!

## Complementary Resources

- Tuto: [Resolving merge conflict](https://docs.github.com/en/github/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)
- Doc: [Advanced Merging](https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging)
- Tuto: [MarkDown Tutorial](https://guides.github.com/features/mastering-markdown/)

## Expected Output

At the end of this challenge you should be **able to use Git collaboratively**, which should be verifiable by each member of your group having a fork of this repository with a `poem.md` file modified by each group member.