# Hike Disaster

You decide to go on a hike in the beautiful Rocky Mountains, but you don't bring
the right gear and things go poorly. You make your way up the mountain, but
sometimes you slide down a slope and have to scramble up again. Every once in a
while you get lucky and find a shortcut.

## Instructions

1. Clone this repository to your computer and navigate to it using your
   terminal.
2. Run `./new-game` in your terminal to begin the game.
3. Run `./next` in your terminal, then move the branch to the indicated commit.
   Repeat this until you complete the hike!

If you make a mistake, you can run `./new-game` to start over.

## Reviewing commit histories

To see details about the commits on your current branch, run `git log`.

There's a commit containing the commits for all 100 places with the tag `list`
that's useful for moving forward. Run `git log list` to see it. 

- You can use `j`/`k` or `Control+d`/`Control+u` to scroll through the history
- Press `q` to quit `git log` and go back to your terminal

## Moving a branch's commit

A Git branch is really just a nickname for a commit. Since every commit keeps
track of the commit that came before it, that one commit is enough to generate
the whole history. 

Use `git reset --hard commit-ref-goes-here` to make the branch
point to that commit.

For example, if you have this commit history:

- `dddd` - "4th commit" - Current
- `cccc` - "3rd commit"
- `bbbb` - "2nd commit"
- `aaaa` - "1st commit"

Running `git reset --hard bbbb` will give you this commit history:

- `bbbb` - "2nd commit" - Current
- `aaaa` - "1st commit"

## Why this matters

Changing a branch's commit is useful for:

- Rolling back to a previous version
- Rolling forward to a successful experiment
- Making one branch the same as another branch

This command is destructive in the sense that it changes the history of the
branch, but note that it doesn't actually delete any commits or work because you
can use `git reflog` and other tools to find commits that aren't in a branch's
history anymore. Commits that aren't being used anywhere are eventually
automatically deleted (90 days by default).

Game 2: [Hike Research](https://github.com/sikaeducation/hike-research)
