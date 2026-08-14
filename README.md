# scaphandre-debian

Debian packaging for [scaphandre](https://github.com/hubblo-org/scaphandre),
published to the [pkg.haus](https://pkg.haus) APT archive.

## Install

Follow the installation instructions on [pkg.haus](https://pkg.haus), then run:

```bash
sudo apt install scaphandre
```

## Building locally

```bash
docker run --rm -v "$PWD:/target" -w /target ghcr.io/pkghaus/deb-builder:trixie
```

Packages land in `debs/`. Build for another suite by swapping the image
tag (`testing` or `unstable`).

## Release

* add a new entry in `debian/changelog`
* update `VERSION` in `package.conf` to the upstream tag
* create a tag matching the Debian package version (`vX.Y.Z-N`) — CI
  validates the build on every suite and architecture; the pkg.haus
  archive ingest builds and publishes it

## License

```
Copyright 2021-2026 pkg.haus

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

```

## Buy me a coffee?

If you feel like buying me a coffee (or a beer?), donations are welcome:

```
BTC : bc1qq04jnuqqavpccfptmddqjkg7cuspy3new4sxq9
DOGE: DRBkryyau5CMxpBzVmrBAjK6dVdMZSBsuS
ETH : 0x2238A11856428b72E80D70Be8666729497059d95
LTC : MQwXsBrArLRHQzwQZAjJPNrxGS1uNDDKX6
```
