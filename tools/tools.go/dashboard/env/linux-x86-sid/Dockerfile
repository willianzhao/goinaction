# Copyright 2014 The Go Authors. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM debian:sid
MAINTAINER golang-dev <golang-dev@googlegroups.com>

ENV DEBIAN_FRONTEND noninteractive

ADD /scripts/install-apt-deps.sh /scripts/
RUN /scripts/install-apt-deps.sh

ADD /scripts/build-go-builder.sh /scripts/
RUN GO_REV=073fc578434b BUILDER_REV=8845ca94a310 /scripts/build-go-builder.sh && test -f /usr/local/bin/builder
