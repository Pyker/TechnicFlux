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
    <a href="https://github.com/Zandercraft/TechnicFlux"><strong>Explore the Docs</strong></a>
    .
    <a href="https://github.com/Zandercraft/TechnicFlux/issues">Report Bug</a>
    .
    <a href="https://github.com/Zandercraft/TechnicFlux/issues">Request Feature</a>
  </p>
</p>

[![Qodana](https://github.com/Zandercraft/TechnicFlux/actions/workflows/qodana_code_quality.yml/badge.svg?branch=dev)](https://github.com/Zandercraft/TechnicFlux/actions/workflows/qodana_code_quality.yml) [![CodeQL](https://github.com/Zandercraft/TechnicFlux/actions/workflows/codeql.yml/badge.svg)](https://github.com/Zandercraft/TechnicFlux/actions/workflows/codeql.yml) [![Contributors](https://img.shields.io/github/contributors/Zandercraft/TechnicFlux?color=dark-green)](https://github.com/Zandercraft/TechnicFlux/graphs/contributors) [![License](https://img.shields.io/github/license/Zandercraft/TechnicFlux)](https://github.com/Zandercraft/TechnicFlux/blob/release/LICENSE.txt) [![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)

## Table Of Contents
* [About the Project](#about-the-project)
* [Built With](#built-with)
* [Getting Started](#getting-started)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Authors](#authors)

## About The Project

![Screen Shot Placeholder](images/screenshot.png)

TechnicFlux is a feature-rich and easy-to-use implementation of the TechnicSolder API including a modern, interactive 
dashboard. 

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
| **Feature**                    | TechnicFlux | TheGameSpider/TechnicSolder | Vanilla TechnicSolder |
|--------------------------------|-------------|-----------------------------|-----------------------|
| Multiple Accounts (with perms) | ✅           | ✅                           | ✅                     |
| Web-based Mod Management       | ✅           | ✅                           | ⚠️ (Limited)*         |
| Web-based Mod Upload           | ✅           | ✅                           | ❌                     |
| Web-based Config Upload        | ✅           | ✅                           | ❌                     |
| Fabric Modloader Support       | ✅           | ✅                           | ⚠️ (Limited)**        |
| Quilt Modloader Support        | ✅           | ⚠️ (Limited)**              | ⚠️ (Limited)**        |
| NeoForge Modloader Support     | ✅           | ⚠️ (Limited)**              | ⚠️ (Limited)**        |
| Modrinth Support               | ✅           | ❌                           | ❌                     |
| Mod Update Tracking***         | ✅           | ❌                           | ❌                     |


**Requires manual zip file construction and an FTP connection to package and upload mods.*  
***Supported by manual zip construction, but not automatic fetch within the web interface.*  
****Via Modrinth's API for mods downloaded from Modrinth only.*


## Built With

TechnicFlux is built using:

* [NodeJS](https://nodejs.org/en)
* [Express](https://www.npmjs.com/package/express)
* [HBS (Handlebars)](https://www.npmjs.com/package/hbs)
* [Morgan](https://www.npmjs.com/package/morgan)
* [Cookie Parser](https://www.npmjs.com/package/cookie-parser)
* [dotenv](https://www.npmjs.com/package/dotenv)
* [bcryptjs](https://www.npmjs.com/package/bcryptjs)
* [mongoose](https://mongoosejs.com/)
* [MongoDB](https://www.mongodb.com/)

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

_For more examples, please refer to the [Documentation](https://example.com)_

## Roadmap

See the [open issues](https://github.com/Zandercraft/TechnicFlux/issues) for a list of proposed features (and known issues).

## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.
* If you have suggestions for adding or removing projects, feel free to [open an issue](https://github.com/Zandercraft/TechnicFlux/issues/new) to discuss it, or directly create a pull request after you edit the *README.md* file with necessary changes.
* Please make sure you check your spelling and grammar.
* Create individual PR for each suggestion.

### Creating A Pull Request

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See [LICENSE.txt](https://github.com/Zandercraft/TechnicFlux/blob/main/LICENSE.txt) for more information.

## Authors

* **Zander** - *([ZandercraftGames](https://github.com/ZandercraftGames/))* - *Project Developer*

## Extra Thanks
> *A special thanks to [TheGameSpider](https://github.com/TheGameSpider) and his [TechnicSolder](https://github.com/TheGameSpider/TechnicSolder)
> implementation for providing an easier way for me to hop into the Minecraft modpack scene. Your enthusiasm for developing
> it and your kindness toward your community really inspired me and showed me what OSS development was all about.*

_We are not affiliated with Mojang, AB or Syndicate LLC._