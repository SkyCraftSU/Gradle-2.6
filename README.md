# Gradle 2.6 — SkyCraft archive

This repository is intended to preserve the **unaltered official Gradle 2.6 binary distribution** for legacy Minecraft 1.7.10 / ForgeGradle 1.2 builds. Gradle itself is developed by [Gradle, Inc. and contributors](https://github.com/gradle/gradle); SkyCraft is not its original developer.

## Release

The GitHub Actions workflow [archive-gradle-2.6.yml](.github/workflows/archive-gradle-2.6.yml) downloads the original Gradle distribution, verifies its SHA-256 checksum (using the upstream checksum file) and ZIP integrity, and publishes it as a GitHub Release asset **only after successful verification**.

After a successful release, the distribution will be at:

https://github.com/SkyCraftSU/Gradle-2.6/releases/download/v2.6/gradle-2.6-bin.zip

**Warning:** GitHub Releases can still redirect to GitHub-hosted file storage. If your network returns HTTP 504 for GitHub release downloads, use a locally cached ZIP or a different accessible artifact mirror; the new release URL does not automatically solve that network issue.

## Usage

In `gradle/wrapper/gradle-wrapper.properties`:

```properties
distributionUrl=https\://github.com/SkyCraftSU/Gradle-2.6/releases/download/v2.6/gradle-2.6-bin.zip
```

Do **not** change the wrapper to this URL before the corresponding release asset actually exists.

No Gradle source files have been modified. This archive is separate from the [SkyCraft ForgeGradle 1.2 fork](https://github.com/SkyCraftSU/ForgeGradle-1.2-SNAPSHOT).
