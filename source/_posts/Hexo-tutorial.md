
---
title: Hexo tutorial
date: 2021-02-17 22:08:28
---

## Prerequesite:
*  This tutorial is based on the MacOS. The steps are similar on other systems.
*  [Node.js](https://nodejs.org/): `node` and `npm` should be installed after installing the `Node.js` package. 
* `sudo -i` or `sudo su` switch to `root` account on your terminal.
*  You can check the their vision by the command `node -v` and `npm -v`.

![](images/16135470990344.png)

## Install Hexo
* `npm install -g hexo-cli` to simply install `hexo`
* `hexo -v` to check the vision of `hexo` as well.
![](images/16135473767369.png)
* Enter your account directory by `cd /User/yourAccountName`, then create and a directory by `mkdir blog`. This directory will save every blog things. Then enter this `blog` directory.
![](images/16135478201958.png)

* `hexo init` to initialise `blog`. Make sure add `sudo` at the front if you are not in `root` account. There are few basic frame content things would be saved in your `blog` directory after initialisation.
![](images/16135481136676.png)

* `hexo s` to start our blog, then `Hexo` will be running at `http://localhost:4000`. Visit this host on your browse, you will see your `Hexo` blog is on and there is a quick start blog `hello-word` on it.
![Screen Shot 2021-02-17 at 15.55.08](Hexo-tutorial/16135460515515/Screen%20Shot%202021-02-17%20at%2015.55.08.png)

* `Ctrl+c` to stop `hexo` and enter `cd source/_posts`, you will see this first blog `hello-world.md` is in there.

## Blog Creation
* `hexo n "YourBlogName"` to crate your blogs and use `vim` or other editors you like to edit your blog. After editing your blog, then back to `blog` diractory.
* `hexo clean` to remove generated files and cache.
* `hexo g` to generate files.
* `hexo s` again, you will find your blogs appear on your hexo blog.
![](images/16135494686637.png)

## Deploy blog to Github

* Create a new repository on Github, and `Repository Name` **must** be `yourGithubAccountName.github.io`. For my example, `hailanggao.github.io`.
![-w767](images/16135512909405.png)

* `npm install --save hexo-deployer-git` to instal `deployer` plug-in under `blog` directory.
![](images/16135501316753.png)
* Now we need to edit `_config.yml` scroll to the end. In `Deployment` section, Edit and save: 

```
deploy:
    type: git
    repo: # your Github repository address (for me: https://github.com/hailanggao/hailanggao.github.io.git)
    branch: master
```
![](images/16135514852166.png)

* `hexo d`, then input your Github account and password to deploy. Mac might ask `Keychain Not Found`, just click `Reset To Defaults` and input your mac password. Then you will find your Github repository appear your generated blog.
![](images/16135517037714.png)
![](images/16135518755765.png)
* You can directly visit your blog by enter your repository name on your browser after deploying.
![-w915](images/16135520183624.png)


## BackUp (Important !!!)

* Use [hexo-git-backup](https://github.com/coneycode/hexo-git-backup) to back up our `hexo` configuration.
* `npm install hexo-git-backup --save` to install `hexo-backup` plug-in.
* Create an branch repository named `backup` on your Github.
* Edit `_config_yml`, add 

```
# Backup
backup:
  type: git
  theme: next, ***  # *** other themes you want to back up, separate by comma
  repo:
    github: ***,backup # replace *** to your backup branch SSH address
```
![](images/16135569491549.png)

* `hexo b` to back up your configurations on your `backup` branch.

 
## Theme and configuration (Option)
* For me: I use [NexT](https://github.com/theme-next/hexo-theme-next) theme.
* `git clone https://github.com/theme-next/hexo-theme-next themes/next` in your `blog` directory. It will save under `/blog/themes`.
![](images/16135524473082.png)

* Back to `blog` directory, edit `_config/yml`. and change `theme: landscape` to `theme: next`. Save and exit, then `hexo clean`(clean), `hexo g`(generate), `hexo s`(start). If everything is ok, `hexo d`(deploy) to deploy.
![](images/16135526686387.png)
-
