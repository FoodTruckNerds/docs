Corepack is a general purpose tool for installing and managing a project's package manager, within the node.js ecosystem.

- If you're a project creator, use the [Leader workflow](#leader-workflow) to set up Corepack for your project.
- If you're a developer coming to a project that has already had Corepack setup, use the [Contributor Setup](#contributor-setup) section.

## Preparation

Due to an issue with [outdated signatures in Corepack](https://github.com/nodejs/corepack/issues/612), Corepack should be updated to its latest version first:

```sh
npm install --global corepack@latest
```

## Leader workflow

Run as Admin in project folder

```sh
corepack enable
```

Installation options:

![](./Pasted%20image%2020250327185946.png)

Set the desired package manager (various examples)

```sh
corepack use pnpm@latest
corepack use pnpm@latest-10
corepack use pnpm@7.x
corepack use pnpm@6.1
corepack use yarn@stable
```

If you want to change package managers, the `use` command above can set a new one.

To download an update for the current package manager, use

```sh
corepack up
```
## Follower Workflow

Run as Admin in project folder

```sh
corepack install
```

The installation process will tell you which package manager is prescribed for use with the project.

## After installation

At this point, you can use the package manager specified by the creator of the project. Since the project has its package dependencies listed in a settings file, you can install all of the dependencies using pnpm, automatically.

```sh
pnpm install
```

The installation procedure will proceed, and a cryptic note at the end will inform you that pnpm is the only package manager allowed to manage the project (courtesy of corepack):

```sh
PS C:\code\amdphreak\ftn-site-vercel> pnpm install
Lockfile is up to date, resolution step is skipped
Already up to date

> food-truck-tracker@1.0.0 preinstall C:\code\amdphreak\ftn-site-vercel
> npx --yes only-allow pnpm

Done in 2.2s using pnpm v10.7.0
```

The output you're seeing indicates that the `pnpm install` command ran successfully, and it included an additional step defined in the project's `preinstall` script.

```sh
> food-truck-tracker@1.0.0 preinstall C:\code\amdphreak\ftn-site-vercel
> npx --yes only-allow pnpm
```

That line indicates that a `preinstall` script in your `package.json` ran automatically as part of the install process. This script runs before `pnpm install` completes and ensures certain conditions are met.
- Specifically, the command `npx --yes only-allow pnpm` runs a package called `only-allow` to enforce that the package manager used for the project is **pnpm**. It prevents the use of other package managers like `npm` or `yarn`.