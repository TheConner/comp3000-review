# COMP3000 Review

Exam review for COMP3000 F19. 
This is built in LaTeX and should require a pretty complete TEX distro to compile. On linux, TeXLive is the way to go. On Windows use MIKTex since it dynamically downloads packages so you don't end up taking up a ton of disk space with packages you don't need.

# Contributing
If you find errors - which is likely since my knowledge of 3000 pretty good but far from perfect - shoot me a message, or if you'd like you can make an account on this GitLab instance and make the changes yourself. 

**Note**: If you want to use git, make an account on this gitlab instance, navigate to this repository then "request access". I'll accept all requests, and then you should be able to merge to the main branch of this repository.

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

## Source Organization

To avoid having one massive blob of a latex document, here's how the sources are organized:
*  **Main Doc**: 3000ExamReview.tex - you should only edit this if you're adding sections
*  **Sections/**: This folder is full of the individual section files that the main doc pulls from. If you want to add a section, add a new file here. Otherwise feel free to edit existing section files with content that is relevant to them. *Note*: section files can contain multiple `\section`s, they just have to fit into the "high level" concept of each section file
*  **questions/**: This folder is where we can put all sample questions / practice questions, and answers. As of writing, I only have some sample questions I wrote for the midterm. I (or someone else) will probably add more questions soon

## Adding a section
1.  Create a new section, say "MySection.tex" in sections
2.  Write some quality content
3.  To see your changes, edit the main doc `3000ExamReview.tex` and add `\input{sections/MySection}` wherever you think the section should go in the main doc. Order does matter here, since the calls to `\input` are done in order
4.  Compile, life should be good!