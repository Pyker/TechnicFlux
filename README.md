<br/>
<p align="center">
  <a href="https://github.com/Zandercraft/TechnicFlux">
    <img src="./public/images/technicflux-logo-white.png" alt="Logo" width="120" height="120">
  </a>

<h3 align="center">TechnicFlux by <a href="https://github.com/Zandercraft">Zandercraft</a></h3>
  <p align="center">
    A feature-rich and easy-to-use implementation of Technic's Solder API using Node.js.
    <br/>
    <br/>
    <a href="https://github.com/Zandercraft/TechnicFlux/wiki"><strong>Explore the Docs</strong></a>
    .
    <a href="https://github.com/Zandercraft/TechnicFlux/issues">Report Bug</a>
    .
    <a href="https://github.com/Zandercraft/TechnicFlux/issues">Request Feature</a>
  </p>
</p>

[![Qodana](https://github.com/Zandercraft/TechnicFlux/actions/workflows/qodana_code_quality.yml/badge.svg?branch=dev)](https://github.com/Zandercraft/TechnicFlux/actions/workflows/qodana_code_quality.yml) [![CodeQL](https://github.com/Zandercraft/TechnicFlux/actions/workflows/codeql.yml/badge.svg)](https://github.com/Zandercraft/TechnicFlux/actions/workflows/codeql.yml) [![Contributors](https://img.shields.io/github/contributors/Zandercraft/TechnicFlux?color=dark-green)](https://github.com/Zandercraft/TechnicFlux/graphs/contributors) [![License](https://img.shields.io/github/license/Zandercraft/TechnicFlux)](https://github.com/Zandercraft/TechnicFlux/blob/release/LICENSE.txt) [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)

> **NOTE:** TechnicFlux is still under active development! Many of the features listed here are not implemented and are
> simply planned for inclusion. We cannot guarantee that everything listed here will eventually be implemented, although
> we will try our best.  
> -- Zander 🙂

## Table Of Contents
* [About the Project](#about-the-project)
  * [What TechnicFlux Isn't](#what-technicflux-is-not)
  * [Why is TechnicFlux Needed?](#why-is-technicflux-needed)
  * [What is TechnicSolder?](#what-is-technicsolder)
  * [How does TechnicFlux compare with TechnicSolder?](#how-does-technicflux-compare-with-technicsolder)
* [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
  * [Contribution Guidelines](./CONTRIBUTING.md)
* [License](#license)
* [Authors](#authors)
* [Extra Thanks](#extra-thanks)

## About The Project

![Screen Shot Placeholder](images/screenshot.png)

TechnicFlux is a feature-rich and easy-to-use implementation of the TechnicSolder API (+ download manager) with a modern,
interactive dashboard. Our aim is to make your job as a modpack developer easy and pain-free while providing you with
some of the best tools to get the job done (such as group-based build access, drag 'n drop mod uploads, and more - see
[How does TechnicFlux compare with TechnicSolder?](#how-does-technicflux-compare-with-technicsolder)).

### What TechnicFlux Is Not
TechnicFlux is quite a few things, but it's important to understand what it is not:
- It is **not** a drag-and-drop replacement for TheGameSpider/TechnicSolder or vanilla TechnicSolder
  - **Explanation:** While we support migration from both vanilla and TheGameSpider's TechnicSolder to aid you in moving
    to TechnicFlux, that's where the support ends. We hope to make your migration as smooth as possible, but do not want to
    constrain ourselves in any way to the feature-set or individual quirks of these applications. (See
    [MIGRATION.md](./MIGRATION.md) for a detailed migration guide).
- It is **not** a PHP application.
  - **Explanation:** TechnicFlux is a Node.js Express application. This means that the way you will deploy it is quite
    different. This has its benefits, but also some drawbacks. For instance, it can be deployed much cheaper and has a lot
    less overhead. It does not, however, run on web servers like Apache or NGINX. You will have to use reverse-proxy for a
    use-case like this.

### Why is TechnicFlux Needed?
After putting days of work into trying to maintain, clean up, and add new features to TheGameSpider/TechnicSolder, I have
come to the realization that it either needs a full re-write or a replacement. Don't get me wrong, I love his version,
have used it for over 5 years now, was a dedicated tester, and finally a major contributor to the project, but with it being
effectively abandoned for the past 3 years, something needs to happen.   
The aim of TechnicFlux is to fill this gap by providing a modern, fast, and easy-to-use project with active, forward-looking
development and support. We hope to maintain this project in a way that the community can actively contribute, get issues
fixed quickly, and have their feedback on new features taken seriously (in much the same way that TheGameSpider handled his
repository in the early stages of the project).

That said, we would just like to thank TheGameSpider for his amazing contributions to the TechnicSolder community, advancing
the technology so much beyond what was available at the time by constantly pioneering new features and making us feel that
our patronage, issues, and feedback really mattered!


### What is TechnicSolder?
> TechnicSolder is an API that sits between a modpack repository and the Technic Launcher. It allows you to easily manage
> multiple modpacks in one single location.
>
> Using Solder also means your packs will download each mod individually. This means the launcher can check MD5's against
> each version of a mod and if it hasn't changed, use the cached version of the mod instead. What does this mean? Small
> incremental updates to your modpack doesn't mean re-downloading the whole thing every time!
>
> Solder also interfaces with the Technic Platform using an API key you can generate through your account there. When
> Solder has this key it can directly interact with your Platform account. When creating new modpacks you will be able
> to import any packs you have registered in your Solder install. It will also create detailed mod lists on your Platform
> page! (assuming you have the respective data filled out in Solder)
>
> *Source: [TechnicPack/TechnicSolder](https://github.com/TechnicPack/TechnicSolder#what-is-solder)*

### How does TechnicFlux compare with TechnicSolder?
| **Feature**                              | **TechnicFlux**              | TheGameSpider/TechnicSolder    | Vanilla TechnicSolder    |
|------------------------------------------|------------------------------|--------------------------------|--------------------------|
| Multiple Accounts (with perms)           | ✅                            | ✅                              | ✅                        |
| Web-based Mod Management                 | ✅                            | ✅                              | ⚠️ (Limited)<sup>1</sup> |
| Drag n' Drop Mod Upload                  | ✅                            | ✅                              | ❌                        |
| Drag n' Drop Config Upload               | ✅                            | ✅                              | ❌                        |
| Forge Modloader Support                  | ✅                            | ✅                              | ⚠️ (Limited)<sup>2</sup> |
| Fabric Modloader Support                 | ✅                            | ✅                              | ⚠️ (Limited)<sup>2</sup> |
| Quilt Modloader Support                  | ✅                            | ⚠️💲 (Limited)<sup>2 & 7</sup> | ⚠️ (Limited)<sup>2</sup> |
| NeoForge Modloader Support               | ✅                            | ⚠️💲 (Limited)<sup>2 & 7</sup> | ⚠️ (Limited)<sup>2</sup> |
| Private Modpack Builds                   | ✅                            | ✅                              | ❌                        |
| Client Groups (e.g. Dev, Testers)        | ✅                            | ❌                              | ❌                        |
| Automatic Mod Info Loading               | ✅                            | ⚠️ (Limited)                   | ❌                        |
| Modrinth Support                         | ✅                            | ❌                              | ❌                        |
| Mod Update Tracking<sup>3</sup>          | ✅                            | ❌                              | ❌                        |
| Custom Modloader Support                 | ⚠️ (Limited)<sup>2 & 4</sup> | ⚠️ (Limited)<sup>2</sup>       | ⚠️ (Limited)<sup>2</sup> |
| Migration from TechnicSolder<sup>5</sup> | ✅                            | ⚠️ (Limited)<sup>6</sup>       | ❌                        |

*<sup>1</sup> Requires manual zip file construction and an FTP connection to package and upload mods.*  
*<sup>2</sup> Supported by manual zip construction, but not automatic fetch within the web interface.*  
*<sup>3</sup> Via Modrinth's API for mods downloaded from Modrinth only.*  
*<sup>4</sup> More support than the others (online configuration w/ mod compatibility).*  
*<sup>5</sup> TechnicFlux supports migration from both Vanilla and TheGameSpider's TechnicSolder.*  
*<sup>6</sup> TheGameSpider's TechnicSolder only supports migration from Vanilla TechnicSolder.*  
*<sup>7</sup> Complete support for this feature will only be available in a closed-source cloud offering of TechnicSolder.*

## Built With

TechnicFlux is built using:

* [NodeJS](https://nodejs.org/en)
* [Express](https://www.npmjs.com/package/express)
* [HBS (Handlebars)](https://www.npmjs.com/package/hbs)
* [Morgan](https://www.npmjs.com/package/morgan)
* [Cookie Parser](https://www.npmjs.com/package/cookie-parser)
* [dotenv](https://www.npmjs.com/package/dotenv)
* [bcryptjs](https://www.npmjs.com/package/bcryptjs)
* [zip.js](https://www.npmjs.com/package/@zip.js/zip.js)
* [mongoose](https://mongoosejs.com/)
* [MongoDB](https://www.mongodb.com/)
* [Bootstrap](https://getbootstrap.com/)

[![js-standard-style](https://cdn.rawgit.com/standard/standard/master/badge.svg)](http://standardjs.com)

## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

You will need the following software to get started:

* [Git](https://git-scm.com/)
* [NodeJS >= 20](https://nodejs.org/en)
* [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
* [MongoDB](https://www.mongodb.com/try/download/community)

### Installation

1. Clone the repo

```sh
git clone https://github.com/Zandercraft/TechnicFlux.git
```

2. Install the project dependencies

```sh
npm install
```

3. Copy and rename the example configuration file

```sh
cp ./.env.example ./.env
```

4. Create a MongoDB database for TechnicFlux to use.

5. Change the values within your .env file to your desired configuration.

6. Run the server
```sh
npm start
```

## Usage

Here are some examples of how you can use TechnicFlux:

(examples)

_For more examples, please refer to the [Documentation](https://github.com/Zandercraft/TechnicFlux/wiki)_

## Contributing

Contributions are what make the open source community such an amazing place to be, learn, inspire, and create. Any
contributions you make are **greatly appreciated**. Our goal as a project is to be open to feedback and contributions,
fostering an active community in which you can truly be involved in improving TechnicFlux and keeping it bug-free.

**See [CONTRIBUTING.md](./CONTRIBUTING.md) for our Contribution Guidelines and more info.**

## License

Distributed under the MIT License.

**See [LICENSE.txt](https://github.com/Zandercraft/TechnicFlux/blob/main/LICENSE.txt) for more information.**

## Authors

* **Zander** - *([ZandercraftGames](https://github.com/ZandercraftGames/))* - *Project Developer*

## Extra Thanks
> *A special thanks to [TheGameSpider](https://github.com/TheGameSpider) and his [TechnicSolder](https://github.com/TheGameSpider/TechnicSolder)
> implementation for providing an easier way for me to hop into the Minecraft modpack scene. Your enthusiasm for developing
> it and your kindness toward your community really inspired me and showed me what OSS development was all about.*

_We are not affiliated with Mojang, AB or Syndicate LLC._