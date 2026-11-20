# VPinPlay

An official extension for [VPinFE](https://github.com/vpinfe/vpinfe). Players, their pictures and accounts, and guests joining from the Remote.

Install it from **System > Extensions** in VPinFE. It is on the [Extension List](https://github.com/vpinfe/extensions).

To write your own extension, see the [extension docs](https://github.com/vpinfe/vpinfe/blob/master/docs/extensions/README.md).

## Running the tests

The tests need a VPinFE checkout, because they drive the real thing. Clone or link this
repository into the checkout's `extensions/vpinplay` folder, then from the checkout's root:

```bash
python -m tests tests/invariants extensions/vpinplay/tests
```

See [Testing your extension](https://github.com/vpinfe/vpinfe/blob/master/docs/extensions/testing.md)
for the rest. `tests/` and `.github/` are left out when VPinFE installs the extension.
