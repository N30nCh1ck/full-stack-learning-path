Go to [[Basic Git]]

#### Handle Merge Conflicted

```Root
|_ repo-1 (git clone <repo> repo-1)
|	|_ index.html
|	|_ styles.css
|_ repo-2 (git clone <repo> repo-2)
	|_ index.html
	|_ styles.css
```

![[vscode-multi-workspace.png]]
you can work 2 repo simultaneously if your screen is large enough, like the above pic.

clone your repo into 2 folder. After finish go to the `repo-1` and change `styles.css` to the following code below.

```css
...
#header {
  ...
  color: tomato;
  font-weight: 600;
}

.paragraph {
  ...
  text-align: justify;
  text-indent: 50px;
  letter-spacing: 3px;
}
...
```

create new branch from `main` branch with `git checkout` then commit your change with message `"change text color and letter spaceing"` or others you want.

go to the `repo-2`  and create new branch from `main` branch with `git checkout` again. update your `styles.css` file by the following code.

```css
...
#header {
  ...
  color: steelblue;
  font-weight: 600;
}

.paragraph {
  ...
  text-align: justify;
  text-indent: 50px;
  letter-spacing: 3px;
}
...
```

commit your code and merge it into `main` branch then push them into *Git Remote*.

come back to your `repo-1` . fetch and pull code from *Git Remote*, especially `main` branch. after that merge your branch into `main` branch and see the result. you are going to face the issue call *"Merge Conflicted"* what you need to do just fix it.

the goal is you *Must* set the `header color` to be `tomato` not `steelblue`. after you already fix it just *Push* the `main` branch into *Git Remote* again.

go to `repo-2` . before using `git fetch` and `git pull`. merge your branch into branch `main`. after that, on branch `main` focus on your `styles.css` at `#header -> color: tomato;` then use git fetch and git pull and see the result.

**Document Hint** 
- [[Basic Git#Clone Git Repo]]
- [[Basic Git#Config Git User]]
- [[Basic Git#Checkout New Branch]]
- [[Basic Git#Add Changed Git]]
- [[Basic Git#Git Commit Message]]
- [[Basic Git#Pushing to Git Remote]]
- [[Basic Git#Check Remote Changes]]
- [[Basic Git#Download Git Remote]]
- [[Basic Git#Merge Git Branch]]