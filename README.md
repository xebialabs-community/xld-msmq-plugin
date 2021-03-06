# xld-msmq-plugin

[![Build Status][xld-msmq-plugin-travis-image]][xld-msmq-plugin-travis-url]
[![License: MIT][xld-msmq-plugin-license-image] ][xld-msmq-plugin-license-url]
[![Github All Releases][xld-msmq-plugin-downloads-image] ]()

[xld-msmq-plugin-travis-image]: https://travis-ci.org/xebialabs-community/xld-msmq-plugin.svg?branch=master
[xld-msmq-plugin-travis-url]: https://travis-ci.org/xebialabs-community/xld-msmq-plugin
[xld-msmq-plugin-license-image]: https://img.shields.io/badge/License-MIT-yellow.svg
[xld-msmq-plugin-license-url]: https://opensource.org/licenses/MIT
[xld-msmq-plugin-downloads-image]: https://img.shields.io/github/downloads/xebialabs-community/xld-msmq-plugin/total.svg


# Introduction

The plugin allows you to define include MSM(Q) Queues Specs in your deployment packages which can deploy to Windows Server environments. 

# Usage

Download the latest plugin from `release` and upload the xldp file to the `XL_DEPLOY_HOME/plugins` directory.

A deployment will look like this:
![deploy](images/deploy.png)

The deployed (queue specification) looks like this:
![deployed](images/deployed.png)

After deployment this package will create the queue in Windows as such:
![queue-in-windows](images/queue-in-windows.png)
![queue-permissions-in-windows](images/queue-permissions-in-windows.png)

# Testing

In order to run this, you should have access to a Windows Server environment with MSMQ installed on it. See [this](https://msdn.microsoft.com/en-us/library/aa967729(v=vs.85).aspx) installation guide on how to install MSMQ to a Windows machine.

By running `./gradlew runDocker` an XL Deploy instance (find the port number in build.gradle, currenlty `4517`) is started with an example setup, expecting a Windows Server on `192.168.56.123`.
