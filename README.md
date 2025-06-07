# Hike Disaster

You decide to go on a hike in the beautiful Rocky Mountains, but you don't bring
the right gear and things go poorly. You make your way up the mountain, but sometimes you slide down a slope and have to scramble up again.

This game is a Git version of Chutes and Ladders that gives you an opportunity
to practice using `git reset --hard` to move the Git HEAD back and forth along a
single branch.

1. Fork and clone this repository
2. Run `./initialize-commits.sh` to set up the project.
3. Run `./new-game` to begin the game.
4. Roll the virtual dice by running `./roll`, then move the current Git HEAD to
   the indicated commit. Repeat until you're on the 100th space.
5. When you get to the 100th space and roll, you've won! Commit `results` and
   push it up to your remote.

## Hints:

- To find the Git hash of the space you want to move to you'll need to run
  `git log list`
  - You can use `j`/`k` and `Control+d`/`Control+u` to scroll Git history
  - Press `q` to quit `git log`
- You can use `git reflog` to see previous commits you've been on
- You can restart the game by running `.new-game` again.

# `git reset --hard` IRL

Game 2: [Hike Research](https://github.com/sikaeducation/hike-research)
