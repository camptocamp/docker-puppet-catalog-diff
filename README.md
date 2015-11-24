Puppet Catalog Diff Docker image
=================================

[![Docker Pulls](https://img.shields.io/docker/pulls/camptocamp/puppet-catalog-diff.svg)](https://hub.docker.com/r/camptocamp/puppet-catalog-diff/)
[![Build Status](https://img.shields.io/travis/camptocamp/docker-puppet-catalog-diff/master.svg)](https://travis-ci.org/camptocamp/docker-puppet-catalog-diff)
[![By Camptocamp](https://img.shields.io/badge/by-camptocamp-fb7047.svg)](http://www.camptocamp.com)


# Usage

```shell
docker run -ti camptocamp/puppet-catalog-diff puppet catalog diff --help
```


## `catalog_diff` wrapper

The image comes with a `catalog_diff` wrapper taking environment variables.

```shell
$ docker run -ti -e "MASTER1=puppet.dev" \
                 -e "MASTER2=puppet.prod" \ # optional, defaults to $MASTER1
                 -e "ENV1=dev" \
                 -e "ENV2=production" \     # optional, defaults to $ENV1
                 -e "PUPPETDB=localhost" \
                 camptocamp/puppet-catalog-diff catalog_diff
```

