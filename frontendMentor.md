# Frontend Mentor Challenges Workflow

## Create Git repo

After unziping the starter files open the project folder with vscode and enter in the terminal:

```bash
git init
```

## First commit

```bash
git add .
git commit -m "Initial commit"
```

## Create GitHub repo

Create a new empty public repo in GitHub and push the existing repo:

```bash
git remote add origin git@github.com:gdsimoes/repo-name.git
git push -u origin main
```

## Set up repo for GitHub pages

Go to the repo settings on GitHub, and then click on `Pages`. On `source` choose `main` as your branch and save. Remember that it can take a few minutes before the website is online.

**Important**: Remember to add a description to the repo and the website.

## Set up Sass

Create a `styles.scss` file (or any other name you like) and then make sass 'watch' the file, i.e., watch the file for changes, and re-compile each time it is necessary:

```bash
sass --watch styles.scss styles.css
```

## Structure HTML

Start by coping (while adapting) the `head` and `footer` section from previous projects. Then, do your best in trying to structure the document while being mindful of the layout. There is no problem with changing it later, so just try not to take too long here.

## Read the style-guide

Read carefully the style guide. Now is a good time to create some Sass variables.

## Do the mobile layout

Create the grid or flexbox layout, set up font families and the colors. Don't worry too much about making everything perfect, like the font sizes.

**Important**: To make the website grow responsively more like a picture you can use `vw` as units. It won't work for monitors with very uncommon sizes. Unfortunately, I don't know how to solve this.

## Do the desktop layout

Before finishing the mobile layout it might be a good idea to start with the desktop one. Then you can dealt with the fonts all at once.

## Finishing up

Remove any cruft, write some comments and write the README.md. If there is anything interactive or animations on the website you should create a gif showing it. It can be done uploading a screen recording to gfycat.
