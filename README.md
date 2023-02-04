<h1 align="center">

<img src="https://raw.githubusercontent.com/Ragdata/Ragdata/master/images/logo/banner/RM-800x400.png" alt="Release Manager" />

[Release Manager v-1.0.0](https://github.com/ragdata/release-manager/releases)
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

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

> Please help me increase signal strength on this repo - give it a ⭐


## 📖 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
  - [Primary Features](#primary-features)
  - [More Detailed Features](#more-detailed-features)
  - [Branch Reliability](#branch-reliability)
- [Global Installation](#-global-installation)
- [Docker Container](#-docker-container)
- [Author/Maintainer](#-author--maintainer)
- [Security](#-security)
- [Available Support](#-available-support)
- [Contributors](#-contributors)
- [Supporting the Project](#-supporting-the-project)
	- [Project Sponsors](#-project-sponsors)
	- [Supporters & Patrons](#-supporters--patrons)
	- [Backers](#-backers)
- [License](#-license)
- [Resources](#-resources)

## ⭐ [Project Overview](#-table-of-contents)

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

[`^ Top`](#-table-of-contents)

## ✨ [Features](#-table-of-contents)

#### [Primary Features](#-table-of-contents)

- Fully Automated Installation!
- Automatically or manually generate the next version number
- Parses git logs looking for commit types configured for display
- Builds **changelog** from git commits using template-defined layouts
- Bumps the version number on files indicated by config file 
- Tags the master branch, ready to deploy your release

#### [More Detailed Features](#-table-of-contents)

- Includes both **Command Line** and **GitHub Actions** versions
- Is fully compatible with [Bash Bits][bash-bits], my modular bash library
- Includes the `bb-logger` logging system from [Bash-Bits][bash-bits]
- Highly customisable using a system of extendable configuration files
- Also includes simple-to-use templates so you can alter the layout of output files
- Is a globally-installed package with a configuration file for each repo
- Can output changelogs in either **Markdown** or **JSON format** - _OR BOTH!_
- Will automatically generate the next version number, or accept one from you

#### [Branch Reliability](#-table-of-contents)

| Branch               |    Stability    | Code Age         | Reliability |
|----------------------|:---------------:|------------------|:-----------:|
| `master`             |  latest stable  | latest release   |     🟢      |
| `develop`            | latest unstable | most recent code |     🔴      |
| `hotfix/*`           |    unstable     | unpredictable    |     🔴      |
| `release/*`          |     stable      | tagged versions  |     🟡      |
| `gh-pages/master`    |  latest stable  | latest release   |     🟢      |
| `gh-pages/develop`   | latest unstable | most recent code |     🔴      |
| `gh-pages/release/*` |     stable      | tagged versions  |     🟡      |

[`^ Top`](#-table-of-contents)

## 📂 [Global Installation](#-table-of-contents)

> This project follows the [Gitflow Workflow][gitflow], so the [`develop branch`][develop] is likely to be in an unstable or even broken state between releases.  Please use the latest [release version][release], or code from the [`master branch`][master] if you want more stable code.

> <p align="center">You can either install Release Manager as a global package on your server,<br>or you can spin up the Docker version  (coming soon) and manage your releases on any system</p>

[`^ Top`](#-table-of-contents)

### [Step 1 - Clone the Repo](#-table-of-contents)

Clone the Release Manager Repo:

```shell
git clone git@github.com:ragdata/release-manager
```

> **NOTE:**
> * If you want to work with the latest, but most unstable code, clone with `--branch develop`
> * If you want to work with the most stable latest release, clone with `--branch master`

### [Step 2 - Setup the Environment](#-table-of-contents)

Enter the directory you cloned the repo to and execute the following command:

```shell
sudo config setup
```

When this step finishes, you'll need to restart your terminal session, and the software will automatically pick up from where it left off and continue:

### [Step 3 - Install the Software](#-table-of-contents)

Kick off the automatic installer with this simple command:

```shell
sudo config install
```

... or if you've already installed the package and only need to update:

```shell
sudo config update
```

[`^ Top`](#-table-of-contents)


## 🐋 [Docker Container](#-table-of-contents)

#### COMING SOON

[`^ Top`](#-table-of-contents)


## 🚧 [Author / Maintainer](#-table-of-contents)

<h3 align="center">
<a href="https://github.com/ragdata" target="_blank"><img src="https://raw.githubusercontent.com/Ragdata/Ragdata/master/images/logo/banner/RedEyed-SW-D-800.png" alt="RedEyed Software" />

Created with ☕ by Ragdata</a>

</h3>

[`^ Top`](#-table-of-contents)

## 🔐 [Security](#-table-of-contents)

While `Release Manager` follows good security practices, 100% security can never be guaranteed in any software package.  `Release Manager` is provided AS IS, and without warranty. You can find more details in the [**LICENSE**](LICENSE) file included with this repository.

If you discover any issue regarding the security of this project, please disclose the information responsibly by sending an email to [`security@ragdata.dev`](mailto:security@ragdata.dev).  Please **DO NOT CREATE AN ISSUE** in the project's Issue Register.  You can read more about this project's security policies [**HERE**](https://github.com/ragdata/release-manager/security/policy) 

[`^ Top`](#-table-of-contents)

## 💪 [Available Support](#-table-of-contents)

<div align="center">

<h3>
<a href="https://github.com/Ragdata/.github/blob/master/.github/SUPPORT.md" target="_blank">Read the Community Support Document</a>

🔸

<a href="https://github.com/ragdata/release-manager/issues" target="_blank">Issues Register</a>
🔸
<a href="https://ragdata.github.io/release-manager" target="_blank">Project Website</a>
🔸
<a href="https://github.com/ragdata/release-manager/discussions" target="_blank">Discussions</a>

🔸

<a href="https://discord.gg/54PkrM7TKq" target="_blank">Join the Discord Server</a>

🔸

Connect with my Social Channels
</h3>

<a href="https://twitter.com/RagdataAU" target="_blank"><img src="https://img.shields.io/badge/Twitter-55ACEE?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter"></a>
<a href="https://reddit.com/r/RedeyedSoftware" target="_blank"><img src="https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white" alt="Reddit"></a>
<a href="https://facebook.com/redeyedsoftware" target="_blank"><img src="https://img.shields.io/badge/Facebook-3B5998?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"></a>
<a href="https://ragdata.substack.com" target="_blank"><img src="https://img.shields.io/badge/Substack-FF6719?style=for-the-badge&logo=substack&logoColor=white" alt="Substack"></a>
<a href="https://discord.gg/54PkrM7TKq" target="_blank"><img src="https://img.shields.io/badge/Discord-7289da?style=for-the-badge&logo=discord&logoColor=white" alt="Substack"></a>

<a href="https://github.com/sponsors/Ragdata" target="_blank"><img src="https://img.shields.io/badge/Sponsors-30363D?style=for-the-badge&logo=github-sponsors&logoColor=EA4AAA" alt="GitHub Sponsors"></a>
<a href="https://patreon.com/ragdata" target="_blank"><img src="https://img.shields.io/badge/Patreon-FF424D?style=for-the-badge&logo=patreon&logoColor=white" alt="Patreon"></a>


</div>

## 💎 [Contributors](#-table-of-contents)

If you'd like to make a contribution of code, then please see my [**Contributor's Guidelines**](https://github.com/Ragdata/.github/blob/master/.github/CONTRIBUTING.md)

It's not just code that I'm looking for though.  If you have any ideas or suggestions about how this project may be improved, don't hesitate to [**open an Issue**](https://github.com/ragdata/release-manager/issues) and let me know!  Because this project follows the [**all-contributors**](https://github.com/all-contributors/all-contributors) specification, contributions of ALL kinds will be recognised here if they are made a part of this project.

#### [View All Contributors][all-contributors]


[`^ Top`](#-table-of-contents)

## 👍 [Supporting the Project](#-table-of-contents)

> Help me increase signal strength on this repo - give it a  ⭐

The creation and maintenance of Open Source Software is definitely a labour of love - this is never going to be a path to riches.  The truth is, it takes not only a lot of time, it creates a substantial amount of personal expense, even when you're working on a shoestring, to keep these projects online and freely available.

If you'd like more info about how you can help out, head to [my sponsor's page][sponsors].

### 🥇 [Project Sponsors](#-table-of-contents)

[FIND OUT ABOUT BECOMING A PROJECT SPONSOR][sponsors]

### 🥈 [Supporters & Patrons](#-table-of-contents)

[FIND OUT ABOUT BECOMING A SUPPORTER OR PATRON][sponsors]

### 🥉 [Backers](#-table-of-contents)

[FIND OUT ABOUT BECOMING A BACKER][sponsors]

[`^ Top`](#-table-of-contents)

[//]: # (## ©️ Copyright & Attributions)

[//]: # ()
[//]: # (This project incorporates ideas and / or code crafted by the following talented individuals:)

[//]: # ()
[//]: # (> "We see much further, and reach much higher,<br>)

[//]: # (> only because we stand upon the shoulders of giants")

[//]: # ()
[//]: # ([`^ Top`]&#40;#-project-overview&#41;)

## 📄 [License](#-table-of-contents)

MIT License

Copyright © 2023 Darren (Ragdata) Poulton

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[`^ Top`](#-table-of-contents)

## 📖 [Resources](#-table-of-contents)

[`^ Top`](#-table-of-contents)

<h2 align="center">
✨ Please help me boost the signal on this project
</h2>


<h3 align="center">

⭐ Star This Repo

<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/ragdata/release-manager?style=social">

<br /><br />

!! SUPPORT THIS REPO !!

<a href="https://github.com/sponsors/ragdata" target="_blank"><img src="https://img.shields.io/badge/support_this_repo-gray?style=for-the-badge&logo=GitHub-Sponsors&logoColor=#white?style=for-the-badge" alt="Support This Repo"></a>

</h3>

<br />
If this project is worth something to you, and you're in a position to be able to help out financially, it would <strong>really</strong> take the pressure off here and allow me to keep working and keep it all freely available!

It doesn't have to be a lot, but you will magnify your contribution if you're able to give a little every month.  If you're not in a position to do that, but think you could make a small, one-time donation to the kitty - you'd be AMAZED how I can make a little go a LONG way!

EVERY financial supporter gets their name associated with the project.

Find out more on my [**Sponsor's Page**][sponsors]

[`^ Top`](#-table-of-contents)

[gitflow]: https://nvie.com/posts/a-successful-git-branching-model/
[develop]: https://github.com/Ragdata/release-manager/tree/develop
[release]: https://github.com/Ragdata/release-manager/releases
[master]: https://github.com/Ragdata/release-manager/tree/master
[bash-bits]: https://github.com/ragdata/bash-bits
[project-site]: https://release-manager.ragdata.dev
[sponsors]: https://github.com/sponsors/ragdata
[commit-types]: https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index
[all-contributors]: CONTRIBUTORS.md