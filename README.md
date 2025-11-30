# libusockets - Debian Package

Debian packaging for µSockets — a minimal cross-platform eventing, networking and cryptography library.

## About µSockets

- **Minimal footprint** async networking library
- **Event loops**: epoll, kqueue, libuv, io_uring, GCD
- **Async networking** with SSL/TLS and QUIC support
- **Apache License 2.0**

**Upstream**: https://github.com/uNetworking/uSockets

## Quick Start

### Installing

```bash
sudo dpkg -i libusockets-dev_*.deb
```

### Building from source

```bash
sudo apt-get install debhelper-compat build-essential libssl-dev libuv1-dev pkg-config
dpkg-source -x libusockets_*.dsc
cd libusockets-*/
dpkg-buildpackage -b -us -uc
sudo dpkg -i ../libusockets-dev_*.deb
sudo apt-get install -f
```

## Package Information

- **Package**: libusockets-dev
- **Version**: 0.8.8-1
- **Maintainer**: Ruslan Dautov
- **Build deps**: debhelper-compat (= 13), libssl-dev, libuv1-dev, pkg-config

## Build Flags

- `WITH_LIBUV=1` — libuv backend
- `WITH_OPENSSL=1` — OpenSSL support 

## Debian Packaging Files

Key packaging files and their purposes:

- **debian/control**: Package metadata and dependencies
- **debian/rules**: Build instructions and configuration
- **debian/copyright**: License and copyright information
- **debian/libusockets-dev.install**: Files to include in the package
- **debian/pkg-config/libusockets.pc**: pkg-config metadata
- **debian/tests/**: Autopkgtest test suite
- **debian/changelog**: Version history
- **debian/watch**: auto tracking of new upstream releases from GitHub

## Contributing

**Debian packaging**:
1. Fork this repository
2. Modify `debian/` directory
3. Update `debian/changelog`
4. Test with `dpkg-buildpackage`
5. Submit a pull request


## License

- **Upstream & Debian packaging**: Apache License 2.0
- See `debian/copyright` for full license info

## Support

- **Packaging issues**: Report here
- **Library issues**: https://github.com/uNetworking/uSockets/issues

---

**Maintainer**: Ruslan Dautov <r.dautoff2016@yandex.ru>