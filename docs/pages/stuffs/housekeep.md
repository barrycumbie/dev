# charlie Solution Walk Through / CodePen to DevBox

1. Get my code from CodePen => Dev Box (dev box = whatever device you are coding on)

- starting from adam
- make sure you are in `editor` view of c/p
- lower left, `export` and choose the `zip` option
- downloads folder... `ctrl + j`
- extracted it, killed my .zip

1. Open is `VS Code`

- file, open folder, select that folder
- gives us this `structure`:

```bash

./
├── dist
│   ├── index.html
│   ├── script.js
│   └── style.css
├── license.txt
├── README.markdown
└── src
    ├── index.html
    ├── script.js
    └── style.css

```

- we'll call this our "starting dir structure"
- `./` = root directory
- sometimes you'll see a folder/dir/subdir referred to with a **whack** after the dir name: `src/`
- do some rearranging:
  - kill `src` `license....` `readme`
  - mv `dist/` up to the `root` and kill the empty `src/`

here's our `intermediate dir structure`

```bash

./
├── index.html
├── script.js
└── style.css

```

- do a lil housekeeping,
  - mv `script.js` and `style.css` into their own subdirs/

looks like this:

```bash

./
├── index.html
├── scripts/
│   └── script.js
└── styles/
    └── style.css

```

:warning: names matter! singular, plural, caps, spaces (don't do spaces)

- make sure our `CODE` matches our directory!
- starting in `index.html` in the `<head>`

```diff

- <link rel="stylesheet" href="./style.css">
+ <link rel="stylesheet" href="./styles/style.css">

```

and also, near the end of `index.html` before the closing `</body>` tag

```diff
- <script  src="./script.js"></script>
+ <script  src="./scripts/script.js"></script>

```
