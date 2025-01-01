# Caddy Buildpack

A Cloud Native Buildpack that installs a custom build of the [Caddy web server](https://caddyserver.com/) with additional modules.

## Features

- Built using Cloud Native Buildpacks specification
- Compatible with Heroku-24 stack
- Includes custom DNS provider modules
- Built with xcaddy for module support

## Included Modules

This buildpack includes Caddy with the following DNS provider modules:
- `github.com/caddy-dns/route53`
- `github.com/caddy-dns/cloudflare`
- `github.com/caddy-dns/digitalocean`
- `github.com/caddy-dns/hetzner`

## Usage

### With pack CLI

    pack build my-app \
    --path . \
    --builder heroku/builder:24 \
    --buildpack https://github.com/blossom-cloud/caddy-buildpack
