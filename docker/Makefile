# Default target executed when no arguments are given to make.

.PHONY: all
all: arch centos debian fedora opensuse ubuntu

.PHONY: arch
arch:
	docker build -t cloudrunnerio/arch:2014.01 arch/2014.01

	docker build -t cloudrunnerio/arch:2014.07 arch/2014.07
	docker tag -f cloudrunnerio/arch:2014.07 cloudrunnerio/arch:latest

.PHONY: centos
centos:
	docker build -t cloudrunnerio/centos:centos6 centos/6

	docker build -t cloudrunnerio/centos:centos7 centos/7
	docker tag -f cloudrunnerio/centos:centos7 cloudrunnerio/centos:latest

.PHONY: debian
debian:
	docker build -t cloudrunnerio/debian:squeeze debian/squeeze

	docker build -t cloudrunnerio/debian:wheezy debian/wheezy

	docker build -t cloudrunnerio/debian:jessie debian/jessie
	docker tag -f cloudrunnerio/debian:jessie cloudrunnerio/debian:latest

.PHONY: fedora
fedora:
	docker build -t cloudrunnerio/fedora:20 fedora/20

	docker build -t cloudrunnerio/fedora:21 fedora/21
	docker tag -f cloudrunnerio/fedora:21 cloudrunnerio/fedora:latest

.PHONY: opensuse
opensuse:
	docker build -t cloudrunnerio/opensuse:bottle opensuse/13.1

	docker build -t cloudrunnerio/opensuse:harlequin  opensuse/13.2
	docker tag -f cloudrunnerio/opensuse:harlequin cloudrunnerio/opensuse:latest

.PHONY: ubuntu
ubuntu:
	docker build -t cloudrunnerio/ubuntu:12.04 ubuntu/12.04

	docker build -t cloudrunnerio/ubuntu:14.04 ubuntu/14.04
	docker tag -f cloudrunnerio/ubuntu:14.04 cloudrunnerio/ubuntu:latest

	docker build -t cloudrunnerio/ubuntu:14.10 ubuntu/14.10

.PHONY: push
push:
	# Arch
	docker push cloudrunnerio/arch

	# Centos
	docker push cloudrunnerio/centos

	# Debian
	docker push cloudrunnerio/debian

	# Fedora
	docker push cloudrunnerio/fedora

	# OpenSUSE
	docker push cloudrunnerio/opensuse

	# Ubuntu
	docker push cloudrunnerio/ubuntu
