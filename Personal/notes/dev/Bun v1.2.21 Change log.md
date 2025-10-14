---
title: "Bun v1.2.21"
source: "https://bun.sh/blog/bun-v1.2.21"
author:
  - "[[Jarred Sumner]]"
published: 2025-08-25
created: 2025-08-25
description: "Fixes 69 issues (addressing 204 👍). Bun.SQL now supports MySQL and SQLite, alongside PostgreSQL. Native YAML support. 500x faster postMessage(string). Bun.build() compile API, with cross-platform targets. Reduced idle CPU usage. Bun.stripANSI for SIMD-accelerated ANSI escape removal. bunx --package flag support. customizable User-Agent headers. Windows executable metadata embedding. and extensive Node.js compatibility improvements"
tags:
  - "clippings"
  - "bun"
  - "ts"
  - "js"
  - "dev"
  - "changelog"
  - "blog"
---
Here's a summary of each major topic from the Bun release notes:

## Bun.SQL - unified SQL client
- New unified API for connecting to MySQL/MariaDB, SQLite, and PostgreSQL databases
- Zero dependencies with native Zig-based MySQL/MariaDB driver
- Same tagged template literal syntax works across all three database types

## Native YAML support
- Built-in YAML parser allowing direct import of `.yaml` and `.yml` files
- Runtime parsing with `Bun.YAML.parse` function
- Works similarly to existing JSON and TOML support

## 500x faster postMessage(string)
- Dramatically improved performance for sending strings between workers
- Also speeds up `structuredClone` for string cloning operations

## Bun.secrets - native secrets manager
- Secure credential storage using OS-native systems (Keychain, GNOME Keyring, Windows Credential Manager)
- Asynchronous operations running in Bun's thread pool
- Designed for CLI tools and local development security

## Security Scanner API for bun install
- Package vulnerability scanning before installation
- Configurable through `bunfig.toml` with npm scanner packages
- Installation cancellation for fatal security vulnerabilities

## bun audit improvements
- New filtering flags: `--audit-level`, `--prod`, `--ignore=<CVE>`
- Better control over security audits and CI/CD integration
- Focus on most critical security issues

## bun install --lockfile-only optimization
- Avoids downloading package tarballs, only fetches manifests
- Significantly reduces bandwidth usage and improves performance
- Still downloads non-npm dependencies as needed

## bun update --interactive enhancements
- Scrolling support for long dependency lists
- Responsive table display that adapts to terminal width
- Better user experience for dependency management

## Reduced idle CPU usage
- Eliminated unnecessary timer for cached Date headers
- Server processes now truly sleep when idle
- Improved resource efficiency

## Bun.build() executable compilation
- Programmatic access to standalone executable creation
- Support for bundler plugins in compiled executables
- New `--compile-exec-argv` flag for embedding runtime arguments

## Windows executable improvements
- Code-signed `bun.exe` to eliminate security warnings
- Metadata embedding support (title, publisher, version, etc.)
- Better Windows integration and user experience

## bunx --package support
- New `--package` flag for running binaries with different names than packages
- Support for scoped packages and multiple binaries
- Brings feature parity with `npx` and `yarn dlx`

## Bun.stripANSI() function
- SIMD-accelerated ANSI escape code removal
- 6x to 57x faster than npm's `strip-ansi` package
- Built-in high-performance alternative

## Additional features
- Glob pattern support in `package.json` sideEffects
- Custom User-Agent flag for HTTP requests
- Extensive Node.js compatibility improvements
- Various bundler, parser, and runtime bug fixes