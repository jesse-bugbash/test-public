# syntax=ghcr.io/reproducible-containers/buildkit-nix:v0.1.1
# Uses a non-standard BuildKit frontend; label PRs should refuse to edit this file.
FROM nixos/nix:2.24.9

COPY flake.nix flake.lock ./
RUN nix build .#default
