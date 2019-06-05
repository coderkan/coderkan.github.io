---
layout: post
title: "GITIGNORE NOT WORKING"
description: "Gitignore general usage."
category: git
modified: 2019-06-06
tags: [git, software, github, gitignore]
imagefeature: Git/gitignore_post/gitignore_notworking.png
share: true
---

<p align="center">
    <img src="{{ site.url }}/images/Git/gitignore_post/gitignore_notworking_lg2.png" width="75%" height="75%">
</p>

Hi everyone,

If you are reading this blog page, you may see that the files you add to the git repos are not ignored by .gitignore.
This is because you don't add the .gitignore file at first.

If you are reading this blog page, you may see that the files you add to the git repos are not ignored by .gitignore.
This is because you don't add the .gitignore file at first, and will cause the files you add to the .gitignore file, 
such as bin, debug, target, etc. to always change. You can see this with the **git status** command.

My colleagues are often confused with this issue. Because they're pretty hasty when you're creating **git repositories**. 
Therefore, they forget to add the .gitignore file at first. 

I dedicate this article to them :)

By making a simple example, I will show you how to solve this situation.

You need to remove tracked files from cache. You can easily do this situation with below command 

* `git rm --cached your_file_name`

After that your `.gitignore` file will work correctly.

I have made a quick video, you can check it out on below.

<p align="center">
	<object width="420" height="315"
		data="https://www.youtube.com/embed/MEmVsyw5rxc">
	</object>
</p>

I hope you enjoy reading.

Have a nice coding…