# Telegraf-SNMP


[
  ![](https://img.shields.io/docker/v/foorschtbar/telegraf-snmp?style=plastic)
  ![](https://img.shields.io/docker/pulls/foorschtbar/telegraf-snmp?style=plastic)
  ![](https://img.shields.io/docker/stars/foorschtbar/telegraf-snmp?style=plastic)
  ![](https://img.shields.io/docker/image-size/foorschtbar/telegraf-snmp?style=plastic)
](https://hub.docker.com/repository/docker/foorschtbar/telegraf-snmp)
[
  ![](https://img.shields.io/github/workflow/status/foorschtbar/telegraf-snmp-docker/Build%20Docker%20Images?style=plastic)
  ![](https://img.shields.io/github/languages/top/foorschtbar/telegraf-snmp-docker?style=plastic)
  ![](https://img.shields.io/github/last-commit/foorschtbar/telegraf-snmp-docker?style=plastic)
  ![](https://img.shields.io/github/license/foorschtbar/telegraf-snmp-docker?style=plastic)
](https://github.com/foorschtbar/telegraf-snmp-docker)

Telegraf Docker Image with Net-SNMP included!

Telegraf is an agent for collecting metrics and writing them to InfluxDB or other outputs. The reason why this image has been forked ([Docker Hub link](https://hub.docker.com/r/foorschtbar/telegraf-snmp/)) is that the official one does not include the SNMP MIBs (used by the `input.snmp` input plugin), it doesnt support ARM architectures and also `config` directory is not specified.

In this fork, three things added:
* Copy modified `entrypoint.sh` to the docker image (by zejdlikt/telegraf-snmp)
* Added `--config-directory` as a startup parameter - you can add configuration files into the `/etc/telegraf/telegraf.d/` folder (by zejdlikt/telegraf-snmp)
* Multiplatform builds for `linux/amd64`, `linux/arm/v7` and `linux/arm64/v8` available

Based on:

* https://www.github.com/nuntz/telegraf-snmp & https://hub.docker.com/r/nuntz/telegraf-snmp/

