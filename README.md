# Better WordPress Plugin Boilerplate ![GitHub contributors](https://img.shields.io/github/contributors/TukuToi/better-wp-plugin-boilerplate) ![GitHub last commit](https://img.shields.io/github/last-commit/TukuToi/better-wp-plugin-boilerplate)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=TukuToi_better-wp-plugin-boilerplate&metric=bugs)](https://sonarcloud.io/dashboard?id=TukuToi_better-wp-plugin-boilerplate) [![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=TukuToi_better-wp-plugin-boilerplate&metric=vulnerabilities)](https://sonarcloud.io/dashboard?id=TukuToi_better-wp-plugin-boilerplate) [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=TukuToi_better-wp-plugin-boilerplate&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=TukuToi_better-wp-plugin-boilerplate) [![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=TukuToi_better-wp-plugin-boilerplate&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=TukuToi_better-wp-plugin-boilerplate) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=TukuToi_better-wp-plugin-boilerplate&metric=security_rating)](https://sonarcloud.io/dashboard?id=TukuToi_better-wp-plugin-boilerplate) [![Run PHPUnit](https://github.com/TukuToi/better-wp-plugin-boilerplate/actions/workflows/phpunit.yml/badge.svg)](https://github.com/TukuToi/better-wp-plugin-boilerplate/actions/workflows/phpunit.yml) [![WordPress Coding Standards](https://github.com/TukuToi/better-wp-plugin-boilerplate/actions/workflows/wpcs.yml/badge.svg)](https://github.com/TukuToi/better-wp-plugin-boilerplate/actions/workflows/wpcs.yml)

The Better WordPress Plugin Boilerplate is a starting point for *developers* looking to create robust and standards-compliant plugins for WordPress and ClassicPress. In a landscape where coding standards and best practices are pivotal, this Boilerplate provides a structured, organized, and modern foundation, ensuring your plugin starts on the right foot.

*If you are not a(n experienced) Developer, you can still use this boilerplate, but there is a learning curve*

## Why This Boilerplate?

- **Modern Codebase:** Crafted with modern PHP practices, this Boilerplate adheres to the latest coding standards, promoting maintainability, scalability, and readability.
- **Adherence to WPCS3** Fully complies with the WordPress Coding Standards v3.
- **Community-Driven:** Born from a desire to continue the legacy of a great project, and to foster collaboration and innovation within the community. The Better WordPress Plugin Boilerplate is not just a code repository, but a hub for developers to share, learn, and contribute.
- **Cross-CMS Compatibility:** Designed with both WordPress and ClassicPress in mind, ensuring a broader reach and future-proofing your plugins against the evolving CMS landscape.
- **Quality Assurance:** With 100% test coverage, WordPress Coding Standards compliance, and continuous scanning by SonarCloud, quality is at the forefront, ensuring your plugins are reliable, secure, and ready for the real world.
- **Educational Value:** Besides being a practical tool, this Boilerplate serves as an educational resource, helping developers understand the best practices in WordPress plugin development.
- **Active Maintenance:** Unlike stagnant boilerplates, the Better WordPress Plugin Boilerplate is under active development. With a growing community and a dedication to accepting and reviewing Pull Requests, this project is continually evolving to include the latest best practices and features.

### Qualities

- **Standardised Package Structure:** Conforms to the [Standard PHP package skeleton](https://github.com/php-pds/skeleton) guidelines, ensuring a consistent and organized package structure.
- **Standardised Code Comments:** Adheres to [phpDocumentor](https://docs.phpdoc.org/guide/guides/docblocks.html) standards for doc block compliant code comments, enhancing code readability and maintainability.
- **Requirement Levels Indications:** Utilizes [RFC-2119](https://datatracker.ietf.org/doc/html/rfc2119) for indicating requirement levels, promoting clear and unambiguous communication of requirements.
- **Object-Oriented PHP and Namespaces:** Employs Object-Oriented PHP and Namespaces to enhance code organization and maintainability, fostering a clean and modular codebase.
- **Test Coverage:** Boasts 100% test coverage with [PHPUnit](https://phpunit.de), ensuring robustness and reliability.
- **WordPress Standard Compliant:** Achieves 100% compliance with [WPCS](https://github.com/WordPress/WordPress-Coding-Standards) `WordPress` Standard, promoting WordPress best practices and coding standards.
- **SonarCloud Scanned:** 100% scanned by [SonarCloud](https://sonarcloud.io/projects), ensuring code quality and identifying potential issues.
- **Fully Documented:** Comprehensive documentation covering all aspects of the boilerplate, facilitating ease of use and customization.
- **Cross-CMS Compatibility:** Ensures 100% compatibility with both WordPress _and_ ClassicPress, catering to a wider developer audience.
- **Security:** Prioritizes security, providing a secure foundation for developing WordPress plugins.

# Usage

This repository is not a Plugin you can download and install. The Plugin files instead are _included_ in the `src` folder of this Repository.

For detailed documentation on the Plugin usage and Development processes, please refer to the [Wiki](https://github.com/TukuToi/better-wp-plugin-boilerplate/wiki).

_Until Wiki is online_
- to manage and release a plugin with this repo/clone of
    - clone/fork this entire repo. Make sure to give the repo the exact name you will want for your _plugin_ (such as `my-awesome-plugin`). The release workflows will use that to zip up your built releases.
	- your _plugin_ will be whatever is inside the root `src` folder. The rest of the root content is NOT part of your plugin, but part of your dev env and workflow
    - develop your plugin by making changes to anything inside the root `src` folder
	- if you need other dependencies add them to the composer file, remove composer lock, and run `composer install`
	- push any changes you make to your `develop` branch
	- this will trigger the wpcs and phpunit workflows, which when passed, allow you to
	- merge your changes to your release branch (typicall `main`)
	- then checkout `main` locally, switch to that branch, and in the CLI run the interactive `/bin/git_release.sh` script
	- this will prompt you a few details and then release your _plugin_ to a new Tag, where an asset will be added that holds your built _plugin_

==> You do NOT need to zip things manually, or run autoloader locally, as the workflows will do that all for you

==> IF you run autoloader manually locally to maybe test your plugin, keep in mind to search-replace the `/src/src/` > `/src/` in the `/src/vendor/composer` files to guarantee no errors. _This step is done for you if you use the release workflow_.


Of course, if this is all too much for you, feel free to just extract `src` contents and use that as your repo, this is entirely up to you.

==> `/bin` includes other helpful scripts to generate documentation of your _plugin_ as well as convert documents from a to another format

# Credits

*This credits section is only here to honor the origins of the repository, as it is a hard-fork. The code has been 100% rewamped from the original.*

## Origins

The WordPress Plugin Boilerplate journey commenced in 2011 with [Tom McFarlin](https://twitter.com/tommcfarlin/) at the helm, later transitioning to [Devin Vinson](https://github.com/DevinVinson) in March 2015. The collaboration included noteworthy contributions from [Josh Eaton](https://twitter.com/jjeaton), [Ulrich Pogson](https://twitter.com/grapplerulrich), and [Brad Vincent](https://twitter.com/themergency).

## Reason for hard-forking 

All the original maintainers are not activly contributing the project anymore, nor willing to let others contribute - **which was made very clear by blocking eager contributors**.

As a growing amount of PRs and requests piled up in the original repository, it became clear that someone needed to continue the work. This hard-fork, now a standalone project, emerged from a desire to propel the original project forward, amidst a prolonged development hiatus on the original repository.

## Curerent situation

Beginning July 5, 2021, the Better WordPress Plugin Boilerplate found a new home with [TukuToi](https://www.tukutoi.com/).

**Our iteration of the Boilerplate not only revives but transcends its predecessor, introducing a plethora of modernized features while retaining a homage to the initial concept and its contributors.** 

The evolution, spurred by community insights and the relentless pursuit of excellence, encapsulates a fresh, modern, and collaborative spirit propelling the WordPress and ClassicPress ecosystems forward.
