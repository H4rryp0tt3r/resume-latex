# My Resume in LaTeX

This needs [BasicTex](https://www.tug.org/mactex/morepackages.html) on MacOS, and also needs a build tool called `ninja` so make sure these are installed.

And for your changes to be reflected on PDF output as in when you change .tex file(Hot reload!).

```bash
ls *.tex | entr ninja
```

The entr command watches for changes in any `.tex` file in this directory and triggers a ninja build when it finds any.
