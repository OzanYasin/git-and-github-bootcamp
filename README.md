# Basics of Github

Github is a hosting platform for git repositories. You can put your own Git repos on Github and access them from anywhere and share them with people around the world.

Beyond hosting repos, Github also provides additional collaboration features that are not native to Git (but are super useful). Basically, Github helps people share and collaborate on repos.

## Difference between Git & Github

**Git** is the version control software that runs locally on your machine. You don't need to register for an account. You don't need the internet to use it. You can use Git without ever touching Github.

**Github** is a service that hosts Git repositories in the cloud and makes it easier to collaborate with other people. You do need to sign up for an account to use Github. It's an online place to share work that is done using Git.

## Collaboration

If you ever plan on working on a project with at least one other person, Github will make your life easier! Whether you're building a hobby project with your friend or you're collaborating with the entire world, Github is essential!

## Open Source Projects

Today Github is THE home of open source projects on the Internet. Projects ranging from React to Swift are hosted on Github.

If you plan on contributing to open source projects, you'll need to get comfortable working with Github.

## Exposure

Your Github profile showcases your own projects and contributions to others' projects.
It can act as a sort of resumé that many employers will consult in the hiring process. Additionally, you can gain some clout on the platform for creating or contributing to popular projects.

## Stay Up to Date

Being active on Github is the best way to stay up to date with the projects and tools you rely on. Learn about upcoming changes and the decisions/debate behind them.

## Cloning

So far we've created our own Git repositories from scratch, but often we want to get a **local copy of an existing repository** instead.

To do this, we can clone a remote repository hosted on Github or similar websites. All we need is a URL that we can tell Git to clone for use.

## Git Clone

To clone a repo, simply run `git clone <url>`.

Git will retrieve all the files associated with the repository and will copy them to your local machine.

In addition, Git initializes a new repository on your machine, giving you access to the full Git history of the cloned project.

> Make sure you are not inside of a repo when you clone!

## Permissions?

**Anyone can clone a repository from Github**, provided the repo is public. You do not need to be an owner or collaborator to clone the repo locally to your machine. You just need the URL from Github.

Pushing up your own changes to the Github repo...that's another story entirely! You need permission to do that!

## SSH Keys

You need to be authenticated on Github to do certain operations, like pushing up code from your local machine. Your terminal will prompt you every single time for your Github email and password, unless...

You generate and configure an SSH key! Once configured, you can connect to Github without having to supply your username/password.

> It's better to read updated guide about how to generate and authenticate SSH keys to your Github profile. Make sure you choose right operator system of yours.

Documents: https://docs.github.com/en/authentication/connecting-to-github-with-ssh

## How Do I Get My Code On Github?

### **Option 1:** Existing Repo

If you already have an existing repo locally that you want to get on Github...

- Create a new repo on Github
- Connect your local repo (add a remote)
- Push up your changes to Github

### **Option 2:** Start From Scratch

If you haven't begun work on your local repo, you can...

- Create a brand new repo on Github
- Clone it down to your machine
- Do some work locally
- Push up your changes to Github
