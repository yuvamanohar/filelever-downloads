# FileLever Downloads

This repository publishes official FileLever release binaries through GitHub
Releases.

Website: https://www.filelever.com

## What FileLever Is

FileLever is a desktop app for local file workflows such as:

- syncing files from one folder to another
- previewing what will be copied, updated, or deleted before running a job
- backing up folder trees to external drives or other locations
- cleaning up file sets with tools that help identify duplicates

The product is designed around local-first file operations. Current releases
focus on the desktop app and macOS packaging.

## What This Repository Contains

This repository is intentionally minimal. It exists to host release artifacts,
checksums, and release notes so users can:

- download a packaged FileLever build
- verify the artifact checksum
- choose the correct build for their machine
- follow release notes for changes and known issues

Download releases here:

- [GitHub Releases](https://github.com/yuvamanohar/filelever-downloads/releases)

## Current Platform Support

Current public releases are provided for macOS only:

- `macos-arm64` for Apple silicon Macs
- `macos-x86_64` for Intel Macs
- `macos-universal2` for a universal build that supports both

If you are not sure which one to choose, download the `macos-universal2`
artifact.

Windows and Linux builds are planned for later releases.

## Release Artifact Naming

FileLever release artifacts follow a strict naming convention.

macOS disk images:

- `FileLever-<version>-macos-arm64.dmg`
- `FileLever-<version>-macos-x86_64.dmg`
- `FileLever-<version>-macos-universal2.dmg`

Checksum manifest:

- `filelever-<version>-sha256.txt`

Example:

- `FileLever-1.0.0-beta.1-macos-arm64.dmg`
- `filelever-1.0.0-beta.1-sha256.txt`

Use the checksum file from the same release as the binary you downloaded.

## How To Download

1. Open the repository's [Releases](https://github.com/yuvamanohar/filelever-downloads/releases) page.
2. Select the latest release or the specific version you want.
3. Under Assets, download the DMG that matches your Mac.
4. Download the matching `filelever-<version>-sha256.txt` file if you want to
   verify integrity.

## How To Verify Checksums

On macOS, open Terminal in your downloads folder and run:

```bash
shasum -a 256 FileLever-<version>-macos-arm64.dmg
```

Then compare the output with the matching line in:

```bash
filelever-<version>-sha256.txt
```

The SHA-256 value must match exactly.

## Installing On macOS

1. Open the downloaded `.dmg`.
2. Drag `FileLever.app` into `Applications`.
3. Open the app from `Applications`.

If macOS warns that the app was downloaded from the internet, use the standard
macOS trust flow:

1. Open `Applications`.
2. Control-click `FileLever.app`.
3. Choose `Open`.
4. Confirm `Open` in the prompt.

## Notes About Releases

- Each GitHub Release may include release notes, version-specific details, and
  known issues.
- Artifact names are versioned so you can keep multiple releases clearly
  separated.
- Checksum manifests are published to make integrity verification simple.
- This repository is for packaged binaries only, not source distribution.

## Support

For release-specific issues, start with the relevant GitHub Release notes in
this repository.
