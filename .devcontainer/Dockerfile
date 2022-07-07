# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.238.0/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT="systemd-20220621"
FROM katsutoshiotogawa/gentoo-stage3-devcontainer:${VARIANT}

RUN emerge-webrsync
RUN emerge -uD @world
RUN emerge app-eselect/eselect-repository
RUN eselect repository enable guru
RUN emerge --sync guru
RUN emerge sys-apps/mlocate

RUN emerge app-arch/rpm
RUN emerge app-arch/rpm2targz

# RUN emerge sys-apps/ripgrep sys-apps/fd
RUN updatedb

