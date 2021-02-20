# Build HTML Emails with rolltop

This package is designed to be used by people with as little comfortability with the command line as possible. That said, it is a command line application and carries with it the associated pitfalls for newcomers. Please feel free to post in the issues of this github repository if you have any difficulty, or suggestions for making the workflow easier.

## Setup

1. Clone this repository

   ~~~bash
   git clone https://github.com/paul-f-maxson/rolltop.git
   ~~~

2. If you haven't already, install homebrew and use it to install pipenv

    ~~~bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ~~~

    ~~~bash
    brew install pipenv
    ~~~

3. Enter the application directory and install package dependencies

    ~~~bash
    cd rolltop
    ~~~

    ~~~bash
    pipenv install
    ~~~

## Usage

Rolltop allows you to design HTML pages in a comfortable environment before converting them to a format that can be sent as emails. Write HTML and CSS in the `src/` directory. `src/index.html` serves as the entry point and is the only required file. Import CSS from this file using `<link>` tags or any other preferred means. For example, `<link rel="stylesheet" href="style.css" />` will apply styles in the file `src/style.css` CSS file to your HTML file.

When you're ready to produce the final email, execute the command `pipenv run build`. This will produce a single file called `index.html` in the `dist/` directory, which can be directly copied into your email. As a convenience, `pipenv run copy` will copy this file to your clipboard. You can also use `pipenv run open` to view the final email in the browser.

## Issues

Feel free to post any issues you have in <https://github.com/paul-f-maxson/rolltop/issues>. Please include a detailed description of your problem inlcuding expected and actual results, along with any error messages.

---
Have fun!
