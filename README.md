# macMAKE v0.1.0 library inputs (local staging)

This folder collects the library inputs referenced by the shipped `examples/first-app` manifest plus the target GCC runtime files already carried in the official macMAKE v0.1.0 archive.

- `msl/`: three Metrowerks MSL archives copied from the local CodeWarrior 8 installation.
- `system-imports/`: CarbonLib and MathLib import stubs from CodeWarrior 8 Universal Interfaces. The complete Universal Interfaces SDK is not copied here; macMAKE registers that SDK by its original root path.
- `gnu-runtime/`: `libgcc.a` and `crtdbase.o` extracted from the checksum-verified macMAKE v0.1.0 archive. The C sample selects `__main.o` and `_ctors.o` from `libgcc.a`; `crtdbase.o` is for the conditional C++ startup path and is not used by that C sample.

The CLI itself does not need the MSL or Apple import files to launch. They are target build inputs. The sample manifest expects the three MSL archives under its project-relative `sdk/` directory; CarbonLib and MathLib are resolved through the registered Universal Interfaces SDK.

## Provenance

- macMAKE release archive: `macmake-v0.1.0-linux-x86_64.tar.xz`
- release archive SHA-256: `3c9da84e53022d16a07208d0591a9964b8399dbe043b3628e227373a6aa6e980`
- release product source revision: `922df8956fb570cdd0a79878904d0bc141141b43`
- source paths and SHA-256 values: `manifest.json` and `SHA256SUMS`

This is a local collection of independently licensed components. The presence of these files here does not change their original license terms or grant public redistribution rights. Review the applicable upstream terms before publishing these files.
