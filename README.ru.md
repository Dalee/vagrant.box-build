# Сборка базовых образов

## Vagrant

 * VirtualBox >= 5.0.12, https://www.virtualbox.org/
 * Vagrant >= 1.7.4, https://www.vagrantup.com/
 * Packer >= 0.8.6, https://www.packer.io/

Сборка осуществляется в автоматическом режиме:

 * CentOS 7.2.1511
 * Debian 8.2.0
 * Ubuntu 14.04.04

```bash
packer build ./centos72.json
packer build ./debian82.json
packer build ./ubuntu14.json
```

### metadata.json

Для автоматического обновления базовых образов необходимо создать файл метаданных.
Примеры метаданных в директории `example/example-metadata.json`

```bash
openssl sha1 ./build/dalee-ubuntu.box
```