## RMG Linux Migration 2014

This is a presentation I gave to the ILRI, Kenya Research Methods Group to prepare them for moving to Linux on their work machines.  I wanted them to understand where Linux came from, and why it's important to use Linux for scientific work.

You can view the presentation on GitHub Pages [here](https://alanorth.github.io/rmg-linux-migration-2014).

### Hacking
If you want to hack on this repo (ie for your own presentation) you will have to clone the repo and then initialize the reveal.js submodule:

    $ git submodule init
    $ git submodule update

Then create a Python virtual environment to setup the required tools for building the presentation:

    $ pyenv virtualenv reveal
    $ pyenv activate reveal
    $ pip install -r requirements.txt

After hacking on the slides in the `source/` directory, build the presentation and start a web server to serve the slides:

    $ fab build
    $ cd presentation
    $ python -m SimpleHTTPServer

The presentation will be available at http://localhost:8000/.

### LICENSE

This repository contains the code of [Reveal.js](https://github.com/hakimel/reveal.js)
which is licensed under the [MIT license](https://github.com/hakimel/reveal.js/blob/master/LICENSE).

Otherwise, the contents of source/ are [Unlicensed](http://unlicense.org/UNLICENSE).
