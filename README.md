# ReadingJournal
This is the base repository for Software Design reading exercises and journal notebooks.

## Active Reading

When learning programming, it's not enough to simply read a textbook. You must be an active reader with hands on keyboards, trying out examples and working through problems as you learn.

In this class, we scaffold this activity through reading journals, implemented as [Jupyter](http://jupyter.org/) notebooks (previously known as ipython notebooks). These allow you to read, take notes, and work through problems, all in one place.

Reading journals must be submitted by pushing to GitHub before noon on the day of the class in which they are due to be considered for credit. We will review work from journals in the next class, so it is not practical to get behind. You are allowed one "free pass" missed submission with no questions asked.


## Get Started Reading

Fork this repository to your personal GitHub account by clicking the "Fork" button in the upper-right corner of the page.

Clone your copy of the repository to your laptop to work on by running the following commands (be sure to replace the username with your own).  These instructions assume that you want to put the Reading Journal in your home directory (~).  If not, make sure to modify the first line to change to the directory where you want your journal to reside.

```
$ cd ~
$ git clone https://github.com/YourUsername/ReadingJournal.git
```

Next, you can fire Jupyter notebook and load the reading journal for day X.

```
$ cd ~/ReadingJournal
$ jupyter notebook dayX_reading_journal.ipynb
```

If all goes well, this should bring up a web-browser with the reading questions as well as an Jupyter notebook you can use for taking your own notes on the reading.


## Submitting Completed Readings

Once you have completed your reading journal (not just the reading exercises, but also your notes as well as any comments you want to give to us), you can turn in your work by running the following commands. First, make sure you have saved the notebook by clicking "Save and checkpoint" in the browser window. Then, run:

```
$ cd ~/ReadingJournal
$ git add dayX_reading_journal.ipynb
$ git commit -m "Turning in my reading journal for day X"
$ git push origin master
```

You will then be prompted to enter your GitHub username and password.  Assuming you followed all of the instructions outlined above, that's it!

## Downloading Future Notebooks

We will continue adding reading notebooks, one per class day, to the original upstream class repository. These will not show up in your forked copy unless you explicitly pull them in.

### One Time Setup: Add Upstream Remote

On your laptop, you should have a cloned copy of the ReadingJournal repository from your GitHub account. You can verify this by checking its remote repositories:

```
$ cd ~/ReadingJournal
$ git remote -v

origin	https://github.com/YourUsername/ReadingJournal.git (fetch)
origin	https://github.com/YourUsername/ReadingJournal.git (push)
```

We want to keep `origin` (the cloned copy in your GitHub account) for you to push completed work to, but we also want to add the original upstream class master repository for you to pull new assignments from. We can add this additional remote by running:

```
$ git remote add upstream	https://github.com/sd16spring/ReadingJournal.git
```

If you run `git remote -v` now, you should see both `origin` and `upstream` listed.

### Pull New Notebooks from Upstream

Each time you want to grab the latest assignments, you should first first make sure all your recent work is committed. This is just to form good habits - each new reading journal assignment will be its own `.ipynb` file, so there should not be any conflicts. Next, run:

```
$ git pull upstream master
```

This should pull in the latest assignment notebook, which you can then complete and push to your `origin` repository by following the usual submission instructions above.

