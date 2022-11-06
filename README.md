# Chapter 11 of Dave Gray's React Tutorial on YT.
Testing to deploy on Netlify and GitHub Pages

See the YT lesson on installing react-icons Chap 7, I think.
Then moving react-icons from dev dependency to prod dependency in Chap 9.
Then proceed to Chap 23.

Couldn't follow the tutorial exactly, since pushing the Chap 11 repo to GH
launches a pop-up, which even if I choose the default nothing happens.
I have to ctrl-C and then just use 'Publish'.

After that, deploying on Netlify is almost the same as the tutorial. Netlify
dialogs had very slight change from the video. It was a successful deploy.

============================================================================

For 23tut-gh OR deploying to the Chapter 11 app to github pages

I 'clone' or created a 'template' of react_deploy_netlify as one cannot fork one's own repository.
Instructions are here: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template

Then I chose 'Create a new repository' , under 'Repository template: Start your repository with a template repository's contents.' choose kwngptrl/react_deploy_netlify.

Under Owner and Repository name: 'kwngptrl/react_deploy_gh'. Then 'Public'

In the next screen is the new repo. Choose 'Code' and copy the address from the pull down menu.

In VSCCode terminal:::::::::::::::::::::::::::::::::::::::::::::

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/01tut (main)
$ cd ..

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series
$ md 23tut-gh
bash: md: command not found				// Oops

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series
$ mkdir 23tut-gh						// Here we go

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series
$ ls
 01tut      react_controlled_inputs-main.zip
 09tut     "README Chapter 7 of Dave Gray's React Tutorial, error.txt"
 10tut     "README Chapter 9 of Dave Gray's React Tutorial, cloning and running 09tut from Dave Gray's repo.txt"
 11tut     "README Chapter 9 of Dave Gray's React Tutorial.txt"
 15tut     'README getting started with CRA with a pristine VSCode.txt'
 16tut     'README using CRA for the Chapter 10 tutotial.txt'
 23tut-gh								// Directory created

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series
$ cd 23tut-gh							// changing over

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh
$ git clone https://github.com/kwngptrl/react_deploy_gh.git			// Cloning it into my react-series folder
Cloning into 'react_deploy_gh'...									// Hmm, it went one folder deeper.
remote: Enumerating objects: 24, done.
remote: Counting objects: 100% (24/24), done.
remote: Compressing objects: 100% (24/24), done.
remote: Total 24 (delta 0), reused 19 (delta 0), pack-reused 0
Receiving objects: 100% (24/24), 293.46 KiB | 2.11 MiB/s, done.

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh
$ ls
react_deploy_gh

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh
$ cd react-deploy-gh												// Oops, should be underscores
bash: cd: react-deploy-gh: No such file or directory

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh
$ cd react_deploy_gh												// I then select and drag this folder from explorer into VSCode's workspace

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ npm i gh-pages -D													// Now following Dave Gray's tutorial
npm WARN deprecated stable@0.1.8: Modern JS already guarantees Array#sort() is a stable sort, so this library is deprecated. See the compatibility table on MDN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#browser_compatibility
npm WARN deprecated w3c-hr-time@1.0.2: Use your platform's native performance.now() and performance.timeOrigin.
npm WARN deprecated svgo@1.3.2: This SVGO version is no longer supported. Upgrade to v2.x.x.

added 1409 packages, and audited 1410 packages in 1m

213 packages are looking for funding
  run `npm fund` for details

6 high severity vulnerabilities

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.										// Edited the package.json etc.

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ git init
Reinitialized existing Git repository in E:/WebDev/react_series/23tut-gh/react_deploy_gh/.git/

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   package-lock.json
        modified:   package.json

no changes added to commit (use "git add" and/or "git commit -a")

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ git add .

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ git commit -m "formal commit, deploying to github pages"
[main f21df6c] formal commit, deploying to github pages
 2 files changed, 334 insertions(+)									// Then from 'Source Control' I 'Sync with origin/main' or something similar, the changes in the lefthand side.
																	// a pop-up will show twice, just press ENTER.
From the terminal:
Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

// Refreshing https://github.com/kwngptrl/react_deploy_gh shows the new changes.

Following the procedure in Dave Gray's tutorial (in the terminal):	// a pop-up menu will show twice, just press ENTER.

Pete@DESKTOP-V0SQTFO MINGW64 /e/WebDev/react_series/23tut-gh/react_deploy_gh (main)
$ npm run deploy

> 11tut@0.1.0 predeploy
> npm run build


> 11tut@0.1.0 build
> react-scripts build

Creating an optimized production build...
Compiled successfully.

File sizes after gzip:

  47.78 kB  build\static\js\main.787ea6b3.js
  860 B     build\static\css\main.d245b3a5.css

The project was built assuming it is hosted at /react_deploy_gh/.
You can control this with the homepage field in your package.json.

The build folder is ready to be deployed.

Find out more about deployment here:

  https://cra.link/deployment


> 11tut@0.1.0 deploy
> gh-pages -d build

Published


// Now go to the package.json where the 'homepage' is specified, which is https://kwngptrl.github.io/react_deploy_gh. Copy and paste that address into a browser. Viola!

In the YouTube page of the tutorial. I posted a question about how Dave grouped the lessons in Chapters and if I had to create-react-app for every chapter going forward. I think this 'template' thing in git will be useful for doing this also. I will have to try sometime.