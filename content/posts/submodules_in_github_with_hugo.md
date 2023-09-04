---
title: "Submodules in Github with Hugo"
date: 2023-09-05T00:30:18+09:00
draft: False
---

## Introduction
I embarked on this journey of using GitHub submodules while setting up my tech blog with Hugo. It was quite the learning curve, but I have managed to grasp the concept fairly well now. For those who are curious, you can check out the repository here: [hugo-blog-awesome](https://github.com/hugo-sid/hugo-blog-awesome).

Here, I am jotting down the process I follow to update submodules, especially when I make changes to the files within them. It's quite a handy note-to-self and perhaps it might assist someone venturing on a similar path.



### Updating Submodules in GiHub: Step-by-Step Guide

1. **Open the Terminal**
I usually start by launching my terminal, either the command prompt or Git Bash on Windows.
<br>
2. **Navigate to My Project Directory**
Next, use the `cd` command to reach project’s main directory. Like this:
   
```sh
cd path/to/my/project
```

3. **Initialize the Submodules**
If you are working with fresh submodules, you will need to initialize them using this command:
```sh
git submodule init
```

4. **Update Submodule**
Then, update the submodule to fetch the latest commits using:
```sh
git submodule update
```

5. **Navigate to the Submodule Directory**
Enter the submodule directory, something like:
```sh
cd path/to/my/submodule
```

6. **Checkout to the Relevant Branch**
I usually switch to the branch where I want to push the updates, typically it's the main branch:
```sh
git checkout main
```

7. **Committing Changes in the Submodule**
Whenever you make changes within the submodule, please make sure to commit those changes at submodule first:
```sh
git add .
git commit -m "Implemented new changes in submodule"
git push
```

8. **Returning to the Main Project Directory**
Then, head back to the main project directory:
```sh 
cd ..
```

9. **Committing and Pushing Changes in the Main Project**
Lastly, I commit and push the changes in the main project to update the submodule reference:
```sh
git add .
git commit -m "Updated submodule with recent changes"
git push
```

## Final Thoughts
This personal guide has been a little savior during my journey of setting up my Hugo tech blog. It might seem a bit overwhelming at first, but with time, it becomes a breeze. Remember, the trick lies in committing changes in the submodule first before updating the main project.

Feel free to explore my Hugo blog repository.