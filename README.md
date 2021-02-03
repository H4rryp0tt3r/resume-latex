# My Resume in LaTeX

This needs [BasicTex](https://www.tug.org/mactex/morepackages.html) on MacOS, and also needs a build tool called `ninja` so make sure these are installed.

And for your changes to be reflected on PDF output as in when you change .tex file(Hot reload!).

```bash
ls *.tex | entr ninja
```

The entr command watches for changes in any `.tex` file in this directory and triggers a ninja build when it finds any. The ninja build produces a file named `resume.pdf`

And for the first time the build may fail, because `resume.tex` file depends on some packages. Use below command when build fails with couldn't find `somepackage.sty`.
Not sure why it need sudo though!(Didn't spend anytime investigating)
```bash
sudo tlmgr install sompackage
```

|Here is the generated output (PDF converted to JPEG for display purpose)|
|------------------------------------------------------------------------|
|![Generated PDF exported as JPEG](https://github.com/H4rryp0tt3r/resume-latex/blob/master/Generated_Resume.jpg)|
