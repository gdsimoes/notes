# Heroku

## Install the Heroku CLI and login

We can use homebrew for that:

```
brew install heroku/brew/heroku
```

And then:

```
heroku login
```

## Create a new Heroku app

Create a file called Procfile containinf the following line:

```
web: npm start
```

Create the .gitignore file with the following line:

```
node_modules
```

We first set up git:

```
cd appFolder
git init
git add .
git commit -m "My first commit"
```

And now Heroku:

```
heroku create
git push heroku main
```
