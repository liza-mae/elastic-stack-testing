# elastic-stack-testing

[WIP] Elastic Stack Testing Framework (ESTF)

This project is a work in progress to provide a common automation framework for elastic stack testing.
<br>The goal is to provide a powerful, easy to use and maintain framework to build test suites.  
<br>One main project for this framework is the development of a product integration test suite.
  - Automated Integration Testing (AIT)

This project is in early stage development and many things are still being ironed out.  

More details can be found:
- [Wiki](https://github.com/elastic/elastic-stack-testing/wiki)
- [Kanban Board](https://github.com/elastic/elastic-stack-testing/projects)

## Infrastructure

 - Software products under test: Elasticsearch, Kibana, Logstash, Beats, Cloud, APM, ML
 - Ansible is used to install and configure the software products under test
 - Python, Pytest and Selenium/Webium will be used for the test framework
 - Automated virtual machine support for Vagrant boxes, AWS EC2 and GCP

## Environment Setup

 * Install Python 3

   In this repo see version file: [**.python-version**](https://github.com/elastic/elastic-stack-testing/blob/master/.python-version)

   https://www.python.org/downloads/

 * Install Vagrant

   In this repo see version: [**.vagrant-version**](https://github.com/elastic/elastic-stack-testing/blob/master/.vagrant-version)

   https://www.vagrantup.com/downloads.html

 * Install Virtualbox

   In this repo see version file: [**.virtualbox-version**](https://github.com/elastic/elastic-stack-testing/blob/master/.virtualbox-version)

   https://www.virtualbox.org/wiki/Downloads

## Quick Start
Running a playbook for provisioning

1. Clone repository: `git clone https://github.com/elastic/elastic-stack-testing.git` 
2. `cd elastic-stack-testing`
3. Select a build URL and switch to the appropriate branch, for example:
   ```
   git checkout 7.16
   export ES_BUILD_URL=artifacts.elastic.co/7.16.3
   ```
4. Run the build: `./buildenv.sh`

For more options see file: `CONTRIBUTING.md`

## Currently Supported

  - Machine: `Vagrant, Virtualbox`
  - Machine OS: `Ubuntu-16.04-x86_64`
  - Node: `Single`
  - Product Versions: `5.6.x, 6.x, 7.x, 8.x`
  - Product Packages: `tar.gz`
  - Product Types: `Regular and OSS`  

## Cloud Environment

  Building the `ci/cloud` project requires a [github API token](https://blog.github.com/2013-05-16-personal-api-tokens/).
  The API key will need repo access (repo checkbox).

  Once a github API token has been acquired three environment variables must be set: `GH_OWNER`, `GH_TOKEN`, and `SDK_VERSION`.

  `GH_OWNER` should be set to `elastic` but can be overridden to your fork if necessary.

  `chmod +x downloadLibs.sh`

  `GH_OWNER=elastic GH_TOKEN=mytoken SDK_VERSION=1.2.0-SNAPSHOT ./downloadLibs.sh`

## Contributing

  Please use the [issue tracker](https://github.com/elastic/elastic-stack-testing/issues) to report any bugs or enhancement requests.  Pull requests are welcome.

## Authors

  Elastic Stack Testing Framework created by [Liza Dayoub](https://github.com/liza-mae).  
  
  Also see a list of [contributors](https://github.com/elastic/elastic-stack-testing/graphs/contributors) who participated in the project.

## License

  Apache License 2.0
