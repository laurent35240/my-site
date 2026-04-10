# my-site

Personal website built with [Hugo](https://gohugo.io/) and hosted on GitHub Pages.

## Local setup

### 1. SSH key

The repo and the `public/` submodule both use the `github.com-laurent35240` SSH alias. Add this to `~/.ssh/config`:

```
Host github.com-laurent35240
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_laurent35240
```

Make sure `~/.ssh/id_rsa_laurent35240` exists and its public key is added to the `laurent35240` GitHub account.

### 2. Clone with submodule

```bash
git clone --recurse-submodules git@github.com-laurent35240:laurent35240/my-site.git
```

If you already cloned without `--recurse-submodules`:

```bash
git submodule update --init
```

### 3. Install Hugo

Requires Hugo **extended** version:

```bash
brew install hugo
```

## Development

```bash
hugo server
```

The site is available at http://localhost:1313.

## Deploy

```bash
./deploy.sh
```

Builds the site into `public/` (the `laurent35240.github.io` submodule) and pushes it to GitHub Pages.
