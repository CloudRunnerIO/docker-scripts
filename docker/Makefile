# Default target executed when no arguments are given to make.

.PHONY: all
all: arch centos debian fedora opensuse ubuntu

.PHONY: arch
arch:
	sudo docker build -t cloudrunnerio/arch:2014.01 arch/2014.01

	sudo docker build -t cloudrunnerio/arch:2014.07 arch/2014.07
	sudo docker tag -f cloudrunnerio/arch:2014.07 cloudrunnerio/arch:latest

.PHONY: centos
centos:
	sudo docker build -t cloudrunnerio/centos:centos6 centos/6

	sudo docker build -t cloudrunnerio/centos:centos7 centos/7
	sudo docker tag -f cloudrunnerio/centos:centos7 cloudrunnerio/centos:latest

.PHONY: debian
debian:
	sudo docker build -t cloudrunnerio/debian:squeeze debian/squeeze

	sudo docker build -t cloudrunnerio/debian:wheezy debian/wheezy

	sudo docker build -t cloudrunnerio/debian:jessie debian/jessie
	sudo docker tag -f cloudrunnerio/debian:jessie cloudrunnerio/debian:latest

.PHONY: fedora
fedora:
	sudo docker build -t cloudrunnerio/fedora:20 fedora/20

	sudo docker build -t cloudrunnerio/fedora:21 fedora/21
	sudo docker tag -f cloudrunnerio/fedora:21 cloudrunnerio/fedora:latest

.PHONY: opensuse
opensuse:
	sudo docker build -t cloudrunnerio/opensuse:bottle opensuse/13.1

	sudo docker build -t cloudrunnerio/opensuse:harlequin  opensuse/13.2
	sudo docker tag -f cloudrunnerio/opensuse:harlequin cloudrunnerio/opensuse:latest

.PHONY: ubuntu
ubuntu:
	sudo docker build -t cloudrunnerio/ubuntu:12.04 ubuntu/12.04

	sudo docker build -t cloudrunnerio/ubuntu:14.04 ubuntu/14.04
	sudo docker tag -f cloudrunnerio/ubuntu:14.04 cloudrunnerio/ubuntu:latest

	sudo docker build -t cloudrunnerio/ubuntu:14.10 ubuntu/14.10

.PHONY: push
push:
	# Arch
	sudo docker push cloudrunnerio/arch:2014.01
	sudo docker push cloudrunnerio/arch:2014.07
	sudo docker push cloudrunnerio/arch:latest

	# Centos
	sudo docker push cloudrunnerio/centos:centos6
	sudo docker push cloudrunnerio/centos:centos7
	sudo docker push cloudrunnerio/centos:latest

	# Debian
	sudo docker push cloudrunnerio/debian:squeeze
	sudo docker push cloudrunnerio/debian:wheezy
	sudo docker push cloudrunnerio/debian:jessie
	sudo docker push cloudrunnerio/debian:latest

	# Fedora
	sudo docker push cloudrunnerio/fedora:20
	sudo docker push cloudrunnerio/fedora:21
	sudo docker push cloudrunnerio/fedora:latest

	# OpenSUSE
	sudo docker push cloudrunnerio/opensuse:bottle
	sudo docker push cloudrunnerio/opensuse:harlequin
	sudo docker push cloudrunnerio/opensuse:latest

	# Ubuntu
	sudo docker push cloudrunnerio/ubuntu:12.04
	sudo docker push cloudrunnerio/ubuntu:14.04
	sudo docker push cloudrunnerio/ubuntu:14.10
	sudo docker push cloudrunnerio/ubuntu:latest
