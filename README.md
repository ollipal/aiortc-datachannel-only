# aiortc-datachannel-only

`aiortc-datachannel-only` is a fork from [aiortc](https://github.com/aiortc/aiortc), which does not require av, cffi or netifaces dependencies, but has a support for datachannels only.

Install with: `pip install aiortc-datachannel-only`

## Why?

- I have only need for datachannels, and I want a simple "pip install ..." to work without extra dependencies or build steps (some others have had the same need, issues [78](https://github.com/aiortc/aiortc/issues/78), [118](https://github.com/aiortc/aiortc/issues/118), [243](https://github.com/aiortc/aiortc/pull/243), [324](https://github.com/aiortc/aiortc/issues/324), [364](https://github.com/aiortc/aiortc/issues/364), [436](https://github.com/aiortc/aiortc/issues/436))
- Netifaces [is no longer maintained](https://github.com/al45tair/netifaces), and does not have binaries for Python3.10

## Caveats:

- This library does not support ipv6 (which the original `aiortc` does support)
- Currently this library uses only the primary ipv4 address (`aiortc` can use all of the ip4 addresses)

## License

`aioice-datachannel-only` is released under the same BSD license as the original `aiortc` library.

## Development

Install: `pip install .[dev]`

Build: `python setup.py bdist_wheel`

Release: `twine upload dist/*` 