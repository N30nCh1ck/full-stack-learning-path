Go to [[📋 Learning Path]]

#### Init Git Repo
create folder then create a file name `index.html` and add the following code.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>Header</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo, non?</p>
  </body>
</html>
```

>Init your Git repository then commit message as "init git repo with index.html"

#### Push Into GitHub
If don't have GitHub go to the link: https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home.

>You can use any type of git cloud such as Gitlab or Bitbucket, but GitHub is a common sense.

#### Clone & Add New Feature
use `git clone` your repository into new directory on your local environment. then create a new branch call "feature" and checkout to the branch you just created one.

update your `index.html` file
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1 id="header">Header</h1>
    <p class="paragraph">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo, non?</p>
  </body>
</html>
```

and add new `styles.css` file
```css
body {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  padding: 20px;
  background-color: #ededed;
}

#header {
  font-size: 32px;
  font-weight: 400;
}

.paragraph {
  font-size: 18px;
  color: #4a4a4a;
}
```

when you finish commit your new branch and push it into GitHub repository.

#### Merge Feature Branch
go to your old directory (the previous one that you have pushed it into git remote at the first time) then fetch your git remote and merge your feature branch into main branch.

once you have merged feature branch push the main branch to your git remote again.

after everything is done. go to another directory then fetch and pull the update on your main branch. you should found the updated `index.html` file and new `styles.css` file like the previous topic. if not you may miss something.


#phase-1 #basic-git #github #gitlab #bitbucket #html #css