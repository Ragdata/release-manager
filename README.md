<h1 align="center">

<img src="https://raw.githubusercontent.com/Ragdata/Ragdata/master/images/logo/banner/RM-800x400.png" alt="Release Manager" />

[Release Manager v-0.1.0](https://github.com/ragdata/release-manager/releases)
</h1>

<h3 align="center"><em>
Ragdata's Release Manager & Changelog Builder
<br /><br />
Includes Command-Line & GitHub Actions Versions
</em><h3>

<h3 align="center">
<a href="https://github.com/ragdata/release-manager/issues">Issues</a>
🔸
<a href="https://github.com/ragdata/release-manager/discussions">Discussions</a>
🔸
<a href="https://github.com/Ragdata/release-manager/releases">Releases</a>

<a href="https://ragdata.github.io/release-manager">Project Site (Documentation)</a>
</h3>

<h4 align="center">Requires Bash4+ & Ubuntu Linux</h4>

## ⭐ Project Overview

> `Release Manager` does exactly what it says on the label, it manages your releases for you but the way it does so is just a little bit special - this software can be used both on the command line or as part of a GitHub Workflow! 

`Release Manager` is comprised of 5 main parts:

**1. Versioner** - the first thing that `Release Manager` needs to do is determine what the next version should be.  You always have the option of telling RM which version to use, but it also has the means to work this out for itself.
<br /><br />
**2. Git Log Parser** - then it automatically grabs every commit record from the git database between the last tagged version and the latest commit which has contains one of the [commit types][commit-types] you have configured to be included in your changelog
<br /><br />
**3. Changelog Builder** - `Release Manager` uses a simple template to group and format those commit messages into an organised and coherent changelog which makes the entire history of your project visible and meaningful
<br /><br />
**4. Version Bumper** - the software then sorts through your git branches and bumps the version number of the files you indicate in the config file and saves those updated files to the appropriate branch waiting for the next step
<br /><br />
**5. Tag Creator** - and finally, `Release Manager` creates a tag of your staging branch with all changes made and committed to the appropriate branches, ready for you to either make manual adjustments to any other files you wanted to include with this **release version** - then all you have to do is deploy your new release!

What happens from here depends on whether you're using the **Command Line Version** of `Release Manager`, or the **GitHub Actions Version**.

## ✨ Features

#### Primary Features

- Fully Automated Installation!
- Automatically or manually generate the next version number
- Parses git logs looking for commit types configured for display
- Builds **changelog** from git commits using template-defined layouts
- Bumps the version number on files indicated by config file 
- Tags the master branch, ready to deploy your release

#### More Detailed Features

- Includes both **Command Line** and **GitHub Actions** versions
- Is fully compatible with [Bash Bits][bash-bits], my modular bash library
- Includes the `bb-logger` logging system from [Bash-Bits][bash-bits]
- Highly customisable using a system of extendable configuration files
- Also includes simple-to-use templates so you can alter the layout of output files
- Is a globally-installed package with a configuration file for each repo
- Can output changelogs in either **Markdown** or **JSON format** - _OR BOTH!_
- Will automatically generate the next version number, or accept one from you


## 📂 Global Installation

> This project follows the [Gitflow Workflow][gitflow], so the [`develop branch`][develop] is likely to be in an unstable or even broken state between releases.  Please use the latest [release version][release], or code from the [`master branch`][master] if you want more stable code.



> <p align="center">You can either install Release Manager as a global package on your server,<br>or you can spin up the Docker version  (coming soon) and manage your releases on any system</p>

### Step 1 - Clone the Repo

Clone the Release Manager Repo:

```shell
git clone git@github.com:ragdata/release-manager
```

> **NOTE:**
> * If you want to work with the latest, but most unstable code, clone with `--branch develop`
> * If you want to work with the most stable latest release, clone with `--branch master`

### Step 2 - Setup the Environment

Enter the directory you cloned the repo to and execute the following command:

```shell
sudo config setup
```

When this step finishes, you'll need to restart your terminal session, and the software will automatically pick up from where it left off and continue:

### Step 3 - Install the Software

Kick off the automatic installer with this simple command:

```shell
sudo config install
```

[`^ Top`](#-project-overview)


## 🐋 Docker Container

#### COMING SOON

[`^ Top`](#-project-overview)


## 🔐 Security

While `Release Manager` follows good security practices, 100% security can never be guaranteed in any software package.  `Release Manager` is provided AS IS, and without warranty. You can find more details in the [LICENSE](LICENSE) file included with this repository.

If you discover any issue regarding the security of this project, please disclose the information responsibly by sending an email to mailto:security@ragdata.dev.  Please DO NOT create an Issue in the project's Issue Register.  You can read more about the project's security policies [HERE](.github/SECURITY.md) 

[`^ Top`](#-project-overview)

## 💪 Available Support

<div align="center">

<h3>
<a href="https://github.com/ragdata/release-manager/issues" target="_blank">Issues Register</a>
🔸
<a href="https://ragdata.github.io/release-manager" target="_blank">Documentation</a>
🔸
<a href="https://github.com/ragdata/release-manager/discussions" target="_blank">Discussions</a>
</h3>

<a href="https://twitter.com/RagdataAU" target="_blank"><img src="https://img.shields.io/badge/Twitter-55ACEE?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter"></a>
<a href="https://reddit.com/RedeyedSoftware" target="_blank"><img src="https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white" alt="Reddit"></a>
<a href="https://facebook.com/redeyedsoftware" target="_blank"><img src="https://img.shields.io/badge/Facebook-3B5998?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"></a>
<a href="https://ragdata.substack.com" target="_blank"><img src="https://img.shields.io/badge/Substack-FF6719?style=for-the-badge&logo=substack&logoColor=white" alt="Substack"></a>
<a href="https://discord.gg/54PkrM7TKq" target="_blank"><img src="https://img.shields.io/badge/Discord-7289da?style=for-the-badge&logo=discord&logoColor=white" alt="Substack"></a>

<a href="https://github.com/sponsors/Ragdata" target="_blank"><img src="https://img.shields.io/badge/Sponsors-30363D?style=for-the-badge&logo=github-sponsors&logoColor=EA4AAA" alt="GitHub Sponsors"></a>
<a href="https://ragdata.patreon.com" target="_blank"><img src="https://img.shields.io/badge/Patreon-FF424D?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"></a>


</div>

## 🚧 Author / Maintainer

<h3 align="center">
<a href="https://github.com/ragdata" target="_blank"><img src="https://raw.githubusercontent.com/Ragdata/Ragdata/master/images/logo/banner/RedEyed-SW-D-800.png" alt="RedEyed Software" />

Created with ☕ by Ragdata</a>

</h3>

[`^ Top`](#-project-overview)

## 💎 Contributors

If you'd like to make a contribution of code, then please see my [Contributor's Guidelines](.github/CONTRIBUTING.md)

It's not just code that I'm looking for though.  If you have any ideas or suggestions about how this project may be improved, don't hesitate to [open an Issue](https://github.com/ragdata/release-manager/issues) and let me know!  Contributions of ALL kinds will be recognised here if they are made a part of this project.


[`^ Top`](#-project-overview)

## 👍 Supporting the Project

> If you've found this or any of my other projects useful in some way and you're motivated to help out, one of the easiest ways to do that is to make sure you give this project a ⭐ - 

The creation and maintenance of Open Source Software is definitely a labour of love - this is never going to be a path to riches.  The truth is, it takes not only a lot of time, it creates a substantial amount of personal expense, even when you're working on a shoestring, to keep these projects online and freely available.   



If you've found this or any of my projects useful in some way and would like to help out, even the smallest of contributions would go a long way towards helping me to keep them freely available to the community.

For more info, head to [my sponsor's page](https://github.com/sponsors/ragdata).

## 🥇 Project Sponsors

## 🥈 Supporters & Patrons


## 🥉 Backers



[`^ Top`](#-project-overview)

## ©️ Copyright & Attributions

This project incorporates ideas and / or code crafted by the following talented individuals:

> "We see much further, and reach much higher,<br>
> only because we stand upon the shoulders of giants"

[`^ Top`](#-project-overview)

## 📄 License

MIT License

Copyright © 2022-2023 Darren Poulton (Ragdata)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


[`^ Top`](#-project-overview)


## 📖 Resources



[`^ Top`](#-project-overview)

[gitflow]: https://nvie.com/posts/a-successful-git-branching-model/
[develop]: https://github.com/Ragdata/release-manager/tree/develop
[release]: https://github.com/Ragdata/release-manager/releases
[master]: https://github.com/Ragdata/release-manager/tree/master
[commit-types]: #-commit-types
[gitflow]: https://nvie.com/posts/a-successful-git-branching-model/
[bash-bits]: https://github.com/ragdata/bash-bits
[project-site]: https://release-manager.ragdata.dev