# satyam1203.github.io

Try deploying react app at username.github.io

### Steps to deploy to `https://username.github.io`:

First of all, create a react-app. We'll create a build for the application everytime a new change is made in default branch and serve using github-pages in that branch.

- Add gh-pages as dev-dependency in you application.
- For this, add required scripts in package.json:
  ```
    "predeploy": "npm run build"
    "deploy": "gh-pages -d build"
  ```
- While pushing any new changes, along with this do `npm run deploy`, this will create a new branch and push the build to the created branch.
- Serve using github-pages at new branch(gh-pages) in /.
- Now, to avoid overhead, add a script `"push": "npm run deploy && git push"` in package.json and after committing, instead of pushing it with `git push`, use `npm run push`.
- Hooray! Visit `https://username.github.io` and your website is live.
