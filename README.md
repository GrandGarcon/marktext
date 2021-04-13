<p align="center"><img src="static/logo-small.png" alt="Mark Text" width="100" height="100"></p>

<h1 align="center">Mark text + JupyterNotebook </h1>

<div align="center">
  <a href="https://twitter.com/intent/tweet?via=marktextme&url=https://github.com/marktext/marktext/&text=What%20do%20you%20want%20to%20say%20to%20app?&hashtags=happyMarkText">
    <img src="https://img.shields.io/twitter/url/https/github.com/marktext/marktext.svg?style=for-the-badge" alt="twitter">
  </a>
</div>
<div align="center">
  <strong>:high_brightness: MD editor functionality combined with jupyter notebook :crescent_moon:</strong><br>
  developing an fork of Mark-text for making light version IDE for writing executable documentations<br>
  <sub>Available for Linux, macOS and Windows.</sub>
</div>

<br>

<div align="center">
  <!-- Version -->
  <a href="https://marktext.github.io/website">
    <img src="https://badge.fury.io/gh/jocs%2Fmarktext.svg" alt="website">
  </a>
  <!-- License -->
  <a href="LICENSE">
    <img src="https://img.shields.io/github/license/marktext/marktext.svg" alt="LICENSE">
  </a>
  <!-- Build Status -->
  <a href="https://travis-ci.org/marktext/marktext/">
    <img src="https://travis-ci.org/marktext/marktext.svg?branch=master" alt="build">
  </a>
  <a href="https://ci.appveyor.com/project/marktext/marktext/branch/master">
    <img src="https://ci.appveyor.com/api/projects/status/l4gxgydj0i95hmxg/branch/master?svg=true" alt="build">
  </a>
  <!-- Downloads total -->
  <a href="https://github.com/marktext/marktext/releases">
    <img src="https://img.shields.io/github/downloads/marktext/marktext/total.svg" alt="total download">
  </a>
  <!-- Downloads latest release -->
  <a href="https://github.com/marktext/marktext/releases/latest">
    <img src="https://img.shields.io/github/downloads/marktext/marktext/v0.16.3/total.svg" alt="latest download">
  </a>
  <!-- sponsors -->
  <a href="https://opencollective.com/marktext">
    <img src="https://opencollective.com/marktext/tiers/silver-sponsors/badge.svg?label=SilverSponsors&color=brightgreen" alt="sponsors">
  </a>
</div>

<div align="center">
  <h3>
    <span> | </span>
    <a href="https://github.com/marktext/marktext#features">
      Features
    </a>
    <span> | </span>
    <a href="https://github.com/marktext/marktext#download-and-installation">
      Downloads
    </a>
    <span> | </span>
    <a href="https://github.com/marktext/marktext#development">
      Development
    </a>
    <span> | </span>
    <a href="https://github.com/marktext/marktext#contribution">
      Contribution
    </a>
  </h3>
</div>


<div align="center">
  <sub>This Markdown editor that could be Jupyter notebooks . enhanced  with ❤︎ by
    <a href="https://github.com/GrandGarcon">Dhruv Malik</a> and upcoming
    <a href="https://github.com/GrandGarcon/marktext/graphs/contributors">
      contributors
    </a>
  </sub>
</div>

<br />

<h2 align="center">Supporting  this project </h2>

Feel free to add the issues and propositions based on the  ISSUE_TEMPLATES present in the .github folder 

## Screenshot

## note : todo for the v0.1 version. 
![](docs/)

## Features

Support for all the major features provided by marktest but includes majorly the following new changes :
- Allowing  running of terminal commands and runtime enviornments for the diffrent code package enviornments (js , python) for better description in the technical documentations . 
- Intellisense support. 
-  working collaboratively with multiple users ( similar to the liveshare).
- And much more .....  
- support of the commands written with `/` . 
So in brief , the aim of the project is to blurr the line between the vscode and the neat markdown application for making an intermediate IDE for 

## Why write another intelligent markdown editor ?

1. To understand the desktop web app developement , along with giving  non expert developers  ,who feel little overwhelmed with the lots of features of vscode ide , to have minimalistic , nice looking editor & at same time getting the 
2. As mentioned above, **Mark Text** is completely free and open source and will be open source forever. We hope that all markdown lovers will contribute their own code and help develop **Mark Text** into a popular markdown editor.
3. There are many markdown editors and all have their own merits, some have features which others don't. It's difficult to satisfy each markdown users' needs but we hope **Mark Text** will be able to satisfy each markdown user as much as possible. Although the latest **Mark Text** is still not perfect, we will try to make it as best as we possibly can.

## Download and Installation

![platform](https://img.shields.io/static/v1.svg?label=Platform&message=Linux-64%20|%20macOS-64%20|%20Win-32%20|%20Win-64&style=for-the-badge)

| ![](https://raw.githubusercontent.com/wiki/ryanoasis/nerd-fonts/screenshots/v1.0.x/mac-pass-sm.png)                                                                                                  | ![](https://raw.githubusercontent.com/wiki/ryanoasis/nerd-fonts/screenshots/v1.0.x/windows-pass-sm.png)                                                                                                          | ![](https://raw.githubusercontent.com/wiki/ryanoasis/nerd-fonts/screenshots/v1.0.x/linux-pass-sm.png)                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| [![latest version](https://img.shields.io/github/downloads/marktext/marktext/latest/marktext.dmg.svg)](https://github.com/marktext/marktext/releases/download/v0.16.3/marktext.dmg) | [![latest version](https://img.shields.io/github/downloads/marktext/marktext/latest/marktext-setup.exe.svg)](https://github.com/marktext/marktext/releases/download/v0.16.3/marktext-setup.exe) | [![latest version](https://img.shields.io/github/downloads/marktext/marktext/latest/marktext-x86_64.AppImage.svg)](https://github.com/marktext/marktext/releases/download/v0.16.3/marktext-x86_64.AppImage) |

## TODO : 
Setting up the changelog  for the initial standards . 

#### macOS

You can either download the latest `marktext-%version%.dmg` from the [release page](https://github.com/marktext/marktext/releases/latest) or install Mark Text using [**homebrew cask**](https://github.com/caskroom/homebrew-cask). To use Homebrew-Cask you just need to have [Homebrew](https://brew.sh/) installed.

```bash
brew install --cask mark-text
```

#### Windows

Simply download and install Mark Text via setup wizard (`marktext-setup-%version%.exe`) and choose whether to install per-user or machine wide.

Alternatively, install Mark Text using [Chocolatey](https://chocolatey.org/). To use Chocolatey you need to have [Chocolatey](https://chocolatey.org/install) installed.

```bash
choco install marktext
```

#### Linux

Please follow the [Linux installation instructions](docs/LINUX.md).

#### Other

All binaries for Linux, macOS and Windows can be downloaded from the [release page](https://github.com/marktext/marktext/releases/latest). If a version is unavailable for your system, then please open an [issue](https://github.com/marktext/marktext/issues).

## Development

If you wish to build **MarkDown IDE** yourself, please check out our [build instructions](docs/dev/BUILD.md).

- [User documentation](docs/README.md)
- [Developer documentation](docs/dev/README.md)

If you have any questions regarding **Mark Text**, you are welcome to write an issue. When doing so please use the default format found when opening an issue. Of course, if you submit a PR directly, it will be greatly appreciated.

## Integrations

- [Alfred Workflow](http://www.packal.org/workflow/mark-text): A Workflow for the macOS app Alfred: Use "mt" to open files/folder with Mark Text.

## Contribution

Mark Text is in full development, please make sure to read the [Contributing Guide](CONTRIBUTING.md) before making a pull request. Want to add some features to Mark Text? Refer to our [roadmap](https://github.com/marktext/marktext/projects) and open issues.

## Contributors

Thank you to all the people who have already contributed to Mark Text[[contributors](https://github.com/marktext/marktext/graphs/contributors)]

Special thanks to @[Yasujizr](https://github.com/Yasujizr) who designed the Mark Text logo.

<a href="https://github.com/marktext/marktext/graphs/contributors"><img src="https://opencollective.com/marktext/contributors.svg?width=890" /></a>

## License

[**MIT**](LICENSE).

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fmarktext%2Fmarktext.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fmarktext%2Fmarktext?ref=badge_large)
