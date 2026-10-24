# Source provenance

## Samsung Open Source listing

The official Samsung Open Source search result for `M127F` lists model `SM-M127F` with firmware versions `M127FXXS9DXJ3` and `M127FXXS9DXJ1` on the same release entry. Its SM-M127F source archive is named `SM-M127F_13_Opensource.zip`.

- Search page: <https://opensource.samsung.com/uploadSearch?searchValue=M127F>
- Device: Samsung Galaxy M12, SM-M127F
- Source archive: `SM-M127F_13_Opensource.zip`
- Package content: `Kernel.tar.gz`, `Platform.tar.gz`, `README_Kernel.txt`, and `README_Platform.txt`
- Kernel build notes identify Android 13, `ARCH=arm64`, and `exynos850-m12nsxx_defconfig`.

The archive used here was supplied by the user. Its filename, contents, and size correspond to the SM-M127F package shown in Samsung's listing. The official listing groups DXJ1 and DXJ3 together; it does not provide a separate DXJ1-only kernel ZIP. Accordingly, this repo records the Samsung package associated with the DXJ1 listing rather than claiming it is a distinct DXJ1-only source snapshot.

## Repository arrangement

The Samsung source archive has been unpacked without editing source files: kernel files are at the repository root, and platform files are under `platform/`. The original `SM-M127F_13_Opensource.zip` is retained as a GitHub Release asset. The user's outer `Download.zip` also contained small M127G/M127N companion files; those unrelated device packages were not imported into this M127F repo.

The SHA-256 values in [`CHECKSUMS.sha256`](CHECKSUMS.sha256) were calculated locally from the supplied source package. They are integrity checks, not a Samsung digital signature or independent proof of the upload's origin.

## Licenses

The downloaded source is provided under the licenses present in its own files. Samsung's download terms additionally state that the source and service are provided “as is” and disclaim warranties. Review the license notices in the tree before reuse or redistribution.
