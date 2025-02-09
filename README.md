# Gogs

[![Build status](https://img.shields.io/travis/gogs/gogs/master.svg?style=for-the-badge&logo=travis)](https://travis-ci.org/gogs/gogs) [![Build status](https://img.shields.io/appveyor/ci/Unknwon/gogs?logo=appveyor&style=for-the-badge)](https://ci.appveyor.com/project/Unknwon/gogs/branch/master) [![Discord](https://img.shields.io/discord/382595433060499458.svg?style=for-the-badge&logo=discord)](https://discord.gg/9aqdHU7) [![Sourcegraph](https://img.shields.io/badge/view%20on-Sourcegraph-brightgreen.svg?style=for-the-badge&logo=sourcegraph)](https://sourcegraph.com/github.com/gogs/gogs)

![](https://github.com/gogs/gogs/blob/master/public/img/gogs-large-resize.png?raw=true)

##### Current tip version: [`.VERSION`](templates/.VERSION) (see [Releases](https://github.com/gogs/gogs/releases) for binary versions)

| Web | UI  | Preview  |
|:-------------:|:-------:|:-------:|
|![Dashboard](https://gogs.io/img/screenshots/1.png)|![Repository](https://gogs.io/img/screenshots/2.png)|![Editor](https://gogs.io/img/screenshots/3.png)|
|![Profile](https://gogs.io/img/screenshots/4.png)|![Diff](https://gogs.io/img/screenshots/5.png)|![Repository Settings](https://gogs.io/img/screenshots/6.png?ts=20170322)|
|![Webhook](https://gogs.io/img/screenshots/7.png)|![Organization](https://gogs.io/img/screenshots/8.png)|![Admin Dashboard](https://gogs.io/img/screenshots/9.png)|

### Important Notes

1. **YOU MUST READ [Contributing Code](https://github.com/gogs/gogs/wiki/Contributing-Code) BEFORE STARTING TO WORK ON A PULL REQUEST**.
2. Due to testing purpose, data of [try.gogs.io](https://try.gogs.io) was reset in **Jan 28, 2015** and will reset multiple times after. Please do **NOT** put your important data on the site.
3. The demo site [try.gogs.io](https://try.gogs.io) is running under `master` branch.
4. If you think there are vulnerabilities in the project, please talk privately to **u@gogs.io**, and the name you want to be credited as. Thanks!
5. If you're interested in using APIs, we have experimental support with [documentation](https://github.com/gogs/go-gogs-client/wiki).
6. If your team/company is using Gogs and would like to put your logo on [our website](https://gogs.io), contact us by any means.

[简体中文](README_ZH.md)

## Vision

This project aims to build a simple, stable and extensible self-hosted Git service that can be setup in the most painless way. With Go, this can be done with an independent binary distribution across **ALL platforms** that Go supports, including Linux, macOS, Windows and ARM.

## Overview

- Please see the [Documentation](https://gogs.io/docs/intro) for common usages and change log.
- Want to try it before doing anything else? Do it [online](https://try.gogs.io/gogs/gogs)!
- Having trouble? Get help with [Troubleshooting](https://gogs.io/docs/intro/troubleshooting.html) or [User Forum](https://discuss.gogs.io/).
- Want to help with localization? Check out the [guide](https://gogs.io/docs/features/i18n.html)!

## Features

- Activity timeline
- SSH and HTTP/HTTPS protocols
- SMTP/LDAP/Reverse proxy authentication
- Reverse proxy with sub-path
- Account/Organization/Repository management
- Add/Remove repository collaborators
- Repository/Organization webhooks (including Slack and Discord)
- Repository Git hooks/deploy keys
- Repository issues, pull requests, wiki and protected branches
- Migrate and mirror repository and its wiki
- Web editor for repository files and wiki
- Jupyter Notebook
- Two-factor authentication
- Gravatar and Federated avatar with custom source
- Mail service
- Administration panel
- Supports MySQL, PostgreSQL, SQLite3, MSSQL and [TiDB](https://github.com/pingcap/tidb) (via MySQL protocol)
- Multi-language support ([30 languages](https://crowdin.com/project/gogs))

## Hardware Requirements

- A Raspberry Pi or $5 Digital Ocean Droplet is more than enough to get you started. Some even use 64MB RAM Docker [CaaS](https://blog.docker.com/2016/02/containers-as-a-service-caas/).
- 2 CPU cores and 512MB RAM would be the baseline for teamwork.
- Increase CPU cores when your team size gets significantly larger, memory footprint remains low.

## Browser Support

- Please see [Semantic UI](https://github.com/Semantic-Org/Semantic-UI#browser-support) for specific versions of supported browsers.
- The smallest resolution officially supported is **1024*768**, however the UI may still look right in smaller resolutions, but no promises or fixes.

## Installation

Make sure you install the [prerequisites](https://gogs.io/docs/installation) first.

There are 6 ways to install Gogs:

- [Install from binary](https://gogs.io/docs/installation/install_from_binary.html)
- [Install from source](https://gogs.io/docs/installation/install_from_source.html)
- [Install from packages](https://gogs.io/docs/installation/install_from_packages.html)
- [Ship with Docker](https://github.com/gogs/gogs/tree/master/docker)
- [Install with Vagrant](https://github.com/geerlingguy/ansible-vagrant-examples/tree/master/gogs)
- [Install with Kubernetes Using Helm Charts](https://github.com/helm/charts/tree/master/incubator/gogs)

### Tutorials

- [How To Set Up Gogs on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-gogs-on-ubuntu-14-04)
- [Run your own GitHub-like service with the help of Docker](http://blog.hypriot.com/post/run-your-own-github-like-service-with-docker/)
- [Dockerized Gogs git server and alpine postgres in 20 minutes or less](http://garthwaite.org/docker-gogs.html)
- [Host Your Own Private GitHub with Gogs](https://eladnava.com/host-your-own-private-github-with-gogs-io/)
- [使用 Gogs 搭建自己的 Git 服务器](https://blog.mynook.info/post/host-your-own-git-server-using-gogs/) (Chinese)
- [阿里云上 Ubuntu 14.04 64 位安装 Gogs](http://my.oschina.net/luyao/blog/375654) (Chinese)
- [Installing Gogs on FreeBSD](https://www.codejam.info/2015/03/installing-gogs-on-freebsd.html)
- [Gogs on Raspberry Pi](http://blog.meinside.pe.kr/Gogs-on-Raspberry-Pi/)
- [Cloudflare Full SSL with Gogs using NGINX](http://www.listekconsulting.com/articles/cloudflare-full-ssl-with-gogs-go-git-service-using-nginx/)

### Screencasts

- [How to install Gogs on a Linux Server (DigitalOcean)](https://www.youtube.com/watch?v=deSfX0gqefE)
- [Instalando Gogs no Ubuntu](https://www.youtube.com/watch?v=4UkHAR1F7ZA) (Português)

### Deploy to Cloud

- [OpenShift](https://github.com/tkisme/gogs-openshift)
- [Cloudron](https://cloudron.io/appstore.html#io.gogs.cloudronapp)
- [Scaleway](https://www.scaleway.com/imagehub/gogs/)
- [Sandstorm](https://github.com/cem/gogs-sandstorm)
- [sloppy.io](https://github.com/sloppyio/quickstarters/tree/master/gogs)
- [YunoHost](https://github.com/YunoHost-Apps/gogs_ynh)
- [DPlatform](https://github.com/j8r/DPlatform)
- [LunaNode](https://github.com/LunaNode/launchgogs)

## Software and Service Support

- [Drone](https://github.com/drone/drone) (CI)
- [Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Gogs+Webhook+Plugin) (CI)
- [Fabric8](http://fabric8.io/) (DevOps)
- [Taiga](https://taiga.io/) (Project Management)
- [Puppet](https://forge.puppetlabs.com/Siteminds/gogs) (IT)
- [Kanboard](http://kanboard.net/plugin/gogs-webhook) (Project Management)
- [BearyChat](https://bearychat.com/) (Team Communication)
- [HiWork](http://www.hiwork.cc/) (Team Communication)
- [GitPitch](https://gitpitch.com/) (Markdown Presentations)

### Product Support

- [Synology](https://www.synology.com) (Docker)
- [One Space](http://www.onespace.cc) (App Store)

## Acknowledgments

- Thanks [Egon Elbre](https://twitter.com/egonelbre) for designing logo.
- Thanks [Crowdin](https://crowdin.com/project/gogs) for sponsoring open source translation plan.
- Thanks [DigitalOcean](https://www.digitalocean.com), [VPSServer](https://www.vpsserver.com/), [Hosted.nl](https://www.hosted.nl/) and [MonoVM](https://monovm.com) for sponsoring VPS services.
- Thanks [KeyCDN](https://www.keycdn.com/) for sponsoring CDN service.
- Thanks [Buildkite](https://buildkite.com) for sponsoring open source CI/CD plan.

## Contributors

- See [contributors page](https://github.com/gogs/gogs/graphs/contributors) for top 100 contributors.
- See [TRANSLATORS](conf/locale/TRANSLATORS) for public list of translators.

## License

This project is under the MIT License. See the [LICENSE](https://github.com/gogs/gogs/blob/master/LICENSE) file for the full license text.

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fgogs%2Fgogs.svg?type=small)](https://app.fossa.io/projects/git%2Bgithub.com%2Fgogs%2Fgogs?ref=badge_small)
