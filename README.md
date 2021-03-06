### Source-to-Image Builder images [![Docker Hub](https://img.shields.io/docker/pulls/fabric8/s2i-java.svg?style=for-the-badge)](https://hub.docker.com/r/fabric8/s2i-java/) [![CircleCI](https://circleci.com/gh/fabric8io-images/s2i.svg?style=svg)](https://circleci.com/gh/fabric8io-images/s2i) 

This repo holds the source for the fabric8's
[S2I](https://docs.openshift.com/enterprise/3.0/creating_images/s2i.html)
builder images for [OpenShift](http://www.openshift.com).


#### Java S2I Builder image

The S2I Java builder can be used to use generate Java S2I builds for
flat classpath applications. It supports flat-classpath and fat-jar packaged applications, leveraging the [run-java-sh project](https://github.com/fabric8io/run-java-sh),
as well as applications using the [hawt-app Maven plugin](https://github.com/fabric8io/fabric8/tree/master/hawt-app-maven-plugin)
for fetching dependencies and building up an appropriate classpath.

#### Karaf S2I Builder image

The Karaf S2I Builder image is used for creating S2I builds for
[Karaf](http://karaf.apache.org/) based applications.


#### Development

##### Release Notes

Please keep the [CHANGELOG.md](CHANGELOG.md) up-to-date.

##### Release Process

Simply creating a tag (and pushing it remote) will [make Circle CI](.circleci/config.yml)
push a release of [fabric8/s2i-java to Docker Hub](https://hub.docker.com/r/fabric8/s2i-java/):

    git tag -a v3.0.0 -m"release v3.0.0
    git push origin v3.0.0

We also automatically publish from the `master` branch to `latest-*` tags.
