# Git Submodule

This repository demonstrates the usage of git submodule. This repository itself can also act as a practice to use git submodule.

## Content

- [Adding Submodule](#Adding-Submodule)
- [Cloning a Repository with Submodules](#Cloning-a-Repository-with-Submodules)
  - [Method 1](#Method-1)
  - [Method 2](#Method-2)
- [Reference](#Reference)

## Adding Submodule

Add a submodule in your git folder by using the command below.  
```bash
git submodule add https://github.com/BruceChanJianLe/git-submodule.git
```

## Cloning a Repository with Submodules

### Method 1

Cloning a git repository with submodules is similar to any other git repository.  
```bash
git clone https://github.com/BruceChanJianLe/git-submodule.git
```

However, you will notice that inside the folder of the submodule is empty. To obtain the content of the submodule please run the command below.  
```bash
# Initialize submodule
git submodule init
# Update submodule
git submodule update
```

**Alternatively**, you may run a single command to perform the above two steps.  
```bash
# This method is preferred
git submodule update --init --recursive
```

### Method 2

This is another method to clone a git repository with submodule if you know the repository has submodule in it before hand.  
```bash
git clone --recurse-submodules
```

## Removing a Submodule

```bash
git submodule deinit <path_to_submodule>
git rm <path_to_submodule>
git commit-m "Removed submodule "
rm -rf .git/modules/<path_to_submodule>
```

## Reference

- Source page [link](https://www.git-scm.com/book/en/v2/Git-Tools-Submodules)
- Video Tutorial [link_youtube](https://www.youtube.com/watch?v=gSlXo2iLBro)
