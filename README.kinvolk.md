# reveal.js Kinvolk theme

[`kinvolk.html`](kinvolk.html) is a [reveal.js](https://github.com/hakimel/reveal.js)
Kinvolk theme.

`index.html` is **not** used in order to easily rebase (w/o managing conflicts)
the master of Kinvolk's fork on upstream/master and stay up-to-date.

## Installation

```
git clone https://github.com/kinvolk/reveal.js my-presentation
cd my-presentation
npm install
```

If you don't have nodejs/npm environment yet, use [`nvm`](https://github.com/creationix/nvm).

## Usage

```
cd my-presentation
echo -e "# My presentation\n\n\n# More content" >slides.md
npm start
# open http://localhost:8000/kinvolk.html in your browser
```

Having reveal.js files mixed with presentation files is not nice. (If there's a
better way with reveal.js, please let me know :) To keep the repository clean,
you can use a subfolder for your presentation files and create a symlink to your
`slides.md`, e.g.

```
mkdir presentation
echo -e "slides.md\npresentation/" >>.git/info/exclude
echo -e "# My presentation\n\n\n# More content" >presentation/slides.md
ln -s presentation/slides.md
npm start
# open http://localhost:8000/kinvolk.html in your browser
```

Caveat: all links have to correctly link to the subdirectory, e.g.

```
<section data-background-image="presentation/graph.svg" data-background-size="contain">
</section>
```

### PDF generation

https://github.com/hakimel/reveal.js#pdf-export

tl;dr: open `http://localhost:8000/kinvolk.html?print-pdf#/` and use Chrome's
print to PDF functionality (`CTRL+p`)

### Speaker notes

Press the `s` key on your keyboard to open the notes window.

https://github.com/hakimel/reveal.js#speaker-notes
