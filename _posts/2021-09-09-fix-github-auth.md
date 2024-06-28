---
layout: post
title: "Fix GitHub Support for password authentication error using Personal Access Token."
subtitle: ""
background: '/img/posts/fix-github-password-auth/bg.jpeg'
---

Installing Github CLI

---
- Ubuntu/Debian
```sh
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```
- Arch
```sh
sudo pacman -S github-cli
```

- Windows

Using WinGet

```sh
winget install gh
```

Using Scoop

```sh
scoop install gh
```

Using Chocolatey

```sh
choco install gh
```
---

Set up github-cli using Personal Access Token

```sh
gh auth login
```
Choose Github.com and proceed to authenticate

Choose HTTPS Protocol and paste authentication token.

Now [create a personal access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token) and paste it.
