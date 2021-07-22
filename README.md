# Cobra - English version
## Updated 06-2021 python3
>
> - updated dependency Werkzeug==0.15.5
> - Fix conflict time.clock
> - Results on webApp translated into English 
> 
## Web Deploy with Conda
> - `conda create --name cobra python=3`
> - `conda activate cobra`
> - `pip install -r requirements.txt`
> - `cp config.template config`
> - `python cobra.py -H 127.0.0.1 -P 5000`

[![Build Status](https://travis-ci.org/WhaleShark-Team/cobra.svg?branch=master)](https://travis-ci.org/WhaleShark-Team/cobra)
[![Coverage Status](https://coveralls.io/repos/github/WhaleShark-Team/cobra/badge.svg?branch=master)](https://coveralls.io/github/WhaleShark-Team/cobra?branch=master)
[![GitHub (pre-)release](https://img.shields.io/github/release/WhaleShark-Team/cobra/all.svg)](https://github.com/WhaleShark-Team/cobra/releases)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/WhaleShark-Team/cobra/blob/master/LICENSE)

[![asciicast](https://raw.githubusercontent.com/WhaleShark-Team/cobra/master/docs/report_03.jpg)](https://asciinema.org/a/132572)

**The project design is no longer able to achieve the current white-box scanning requirements, and is no longer being maintained for research use only, please do not use it in a production environment**

## Introduction
Cobra is a **source code security audit** tool that supports detection of **most significant** security issues and vulnerabilities in source code of multiple development languages.

## Features
#### Multi-language Supported (support for multiple development languages)
> Supports development languages such as PHP, Java, and dozens of types of files.

#### Multi-Vulnerabilities Supported (support for multiple vulnerability types)
> The first batch of tens of thousands of insecure dependency checking rules and dozens of code security scanning rules are open, and more scanning rules will continue to be opened later.

#### GUI/CLI/API Mode (command line mode and API mode)
> Provide local Web Server service, can use GUI visual operation, also can support local API interface, convenient and other systems (release system, CI, etc.) docking extension.

## Screenshot
Screenshot [! [report01](https://raw.githubusercontent.com/whaleshark-team/cobra/master/docs/report_01.jpg)](https://whaleshark-team.github.io/ cobra/api)
[! [report02](https://raw.githubusercontent.com/whaleshark-team/cobra/master/docs/report_02.jpg)](https://whaleshark-team.github.io/ cobra/api)

## Contributors
The project was initiated and led by [Feei](https://github.com/FeeiCN), with core developers [LiGhT1EsS](https://github.com/LiGhT1EsS), [BlBana](https://github.com/BlBana), [ 40huo](https://github.com/40huo), [braveghz](https://github.com/braveghz), and also thanks to other [contributors](https://github.com/WhaleShark-Team/cobra/ graphs/contributors), feel free to submit PRs.

## Links
- [Cobra Documentation](https://whaleshark-team.github.io/cobra/