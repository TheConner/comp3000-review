# COMP3000 Review

Exam review for COMP3000 F19. 
This is built in LaTeX and should require a pretty complete TEX distro to compile. On linux, TeXLive is the way to go. On Windows use MIKTex since it dynamically downloads packages so you don't end up taking up a ton of disk space with packages you don't need.

# Contributing
If you find errors - which is likely since my knowledge of 3000 pretty good but far from perfect - shoot me a message, or if you'd like you can make an account on this GitLab instance and make the changes yourself.

If you're not familiar with Git or LaTeX, I'll happily make the changes for you. DM me with issues, additions, philosophical thoughts on life, etc, or if you'd like your efforts to be tracked make an account on this gitlab instance and submit an issue request on this repository.

# Getting the sources and Building

Clone this repository, 
```bash
$ git clone http://gitlab.advtech.ca/netwinder/comp3000-review.git
$ cd comp3000-review
$ pdflatex 3000ExamReview.tex
```
Any latex editor should build the main file 3000ExamReview without issues.

Bear in mind that this should build with a fairly complete latex distro, and you should be building to PDF *not* to DVI. If you're having issues building shoot me a message.

If you're not familiar with latex, consider the following editors / IDEs:

- Vim-latex if you are a vim user
- TeXStudio / TeXMaker if you value your sanity
- Emacs + auctex for those who use emacs
- I hear there's addons for VS code if you enjoy the "open source" (but not really open source) editor.

