# project_creativecommons.org

Project to manage technical implementation of [creativecommons.org](https://creativecommons.org/) (primary website)


## Status

1. Website: **Pre-release**
   - (For current/legacy repositories, see: [creativecommons/creativecommons.org](https://github.com/creativecommons/creativecommons.org): Website parent project, legalcode and translations, and GitHub Issues for public help and support)
2. Repository:
   - Legal Tools not yet incorporated into this project's docker configuration
   - Misc Resources not yet incorporated into this project's docker configuration


## Overview

This repository manages the primary website ([creativecommons.org](https://creativecommons.org/)) project. The primary website consists of the following components and repositries:
1. WordPress
   - [creativecommons/creativecommons-base](https://github.com/creativecommons/creativecommons-base): Base WordPress theme for Creative Commons websites.
     - [creativecommons/wp-theme-creativecommons.org](https://github.com/creativecommons/wp-theme-creativecommons.org): New WordPress theme for Creative Commons website
2. Legal Tools
   - [creativecommons/chooser](https://github.com/creativecommons/chooser/): [WIP] The new and improved CC license selection tool.
   - [creativecommons/cc-licenses](https://github.com/creativecommons/cc-licenses): New license infrastructure for Creative Commons
   - [creativecommons/cc-licenses-data](https://github.com/creativecommons/cc-licenses-data): CC Licenses data (static HTML, language files, etc.)
3. Misc Resources
   - [creativecommons/faq](https://github.com/creativecommons/faq): Creative Commons FAQ page
   - [creativecommons/mp](https://github.com/creativecommons/mp): Documentation for CC integration into user-generated content platforms

Infrastructure Management is handled by:
- [creativecommons/sre-salt-prime](https://github.com/creativecommons/sre-salt-prime/): Site Reliability Engineering / DevOps SaltStack configuration files


## Code of Conduct

[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md):
> The Creative Commons team is committed to fostering a welcoming community.
> This project and all other Creative Commons open source projects are governed
> by our [Code of Conduct][code_of_conduct]. Please report unacceptable
> behavior to [conduct@creativecommons.org](mailto:conduct@creativecommons.org)
> per our [reporting guidelines][reporting_guide].

[code_of_conduct]:https://creativecommons.github.io/community/code-of-conduct/
[reporting_guide]:https://creativecommons.github.io/community/code-of-conduct/enforcement/


## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) and [Contributors ✨](#contributors-), below.


## Prerequisites

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->


## Development


### Development dependencies
Make sure you have installed [node/npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm), [Docker](https://docs.docker.com/get-docker/), and `docker-compose` for your operating system prior to following these instructions.

We are using the [`wordpress/env` project](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-env/) to simplify our developer experience. Please follow the `wordpress/env` installation instructions.


### Initialize Git submodules

This project consists of several components, such as WordPress themes, that are developed in their own Git repositories. If you have already cloned this project's code, make sure the Git sub-modules are activated by running the following command.

```sh
git submodule update --init
```

Alternatively, you can initialize the submodules when you clone the repository with the following command.

```sh
git clone --recursive
```


### Run the development server

Once you have installed the above development dependencies, you can run the following commands from within this project directory.


#### Start the server

```sh
wp-env start
```

**Note:** if you get an [error related to Xdebug when starting the server](https://github.com/WordPress/gutenberg/issues/34320), make sure to prune old Docker images with

```
docker image prune -a
```


#### Stop the server

```sh
wp-env stop
```


### Log in to WordPress

With the development server running, log in to the local WordPress with the default login credentials.

- username: admin
- password: password


## License

- [`LICENSE`](LICENSE) (Expat/[MIT][mit] License)

[mit]: http://www.opensource.org/licenses/MIT "The MIT License | Open Source Initiative"


## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://www.epacking.be"><img src="https://avatars.githubusercontent.com/u/19891785?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Alain Seys</b></sub></a><br /><a href="https://github.com/creativecommons/project_creativecommons.org/commits?author=alainseys" title="Code">💻</a> <a href="#infra-alainseys" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="https://github.com/creativecommons/project_creativecommons.org/commits?author=alainseys" title="Documentation">📖</a></td>
    <td align="center"><a href="http://linkedin.com/in/brylie-christopher-oxley/"><img src="https://avatars.githubusercontent.com/u/17307?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Brylie Christopher Oxley</b></sub></a><br /><a href="https://github.com/creativecommons/project_creativecommons.org/commits?author=brylie" title="Code">💻</a> <a href="https://github.com/creativecommons/project_creativecommons.org/pulls?q=is%3Apr+reviewed-by%3Abrylie" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/creativecommons/project_creativecommons.org/issues?q=author%3Abrylie" title="Bug reports">🐛</a> <a href="https://github.com/creativecommons/project_creativecommons.org/commits?author=brylie" title="Documentation">📖</a></td>
    <td align="center"><a href="https://zehta.me/"><img src="https://avatars.githubusercontent.com/u/691322?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Timid Robot Zehta</b></sub></a><br /><a href="https://github.com/creativecommons/project_creativecommons.org/pulls?q=is%3Apr+reviewed-by%3ATimidRobot" title="Reviewed Pull Requests">👀</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
