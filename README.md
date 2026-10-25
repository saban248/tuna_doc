# tuna_doc
## Windows Malware Research — Architecture Documentation

`tuna_doc` is a documentation-oriented repository for a privately maintained Windows malware research project. It publishes selected C++ headers and interface declarations to illustrate the project's organization without publishing the full implementation or its private server.

> **Important:** This is an interface/documentation snapshot, not a complete or buildable source release. Function declarations describe intended interfaces; they do not independently verify runtime behavior.

## Purpose

The repository provides a limited view of the project's software structure for portfolio and research-documentation purposes. The implementation files and private server are intentionally not included.

## What is included

- C++ header files with declarations, signatures, comments, and selected class interfaces.
- `tunax1.cpp`, which shows the program entry point and top-level object initialization.
- `trojan_project.pdf`, a concise lifecycle/architecture diagram.
- `stb_image.h` and `stb_image_write.h`, third-party image-processing headers attributed in the original project to Sean T. Barrett and the [stb project](https://github.com/nothings/stb).

## High-level component map

The following is inferred from the published filenames and header comments; it describes declared responsibilities, not verified runtime behavior.

| File | Declared area |
|---|---|
| `analyze.h` | System information helpers, string/byte transformations, and packet-structure declarations |
| `explorer.h` | Windows filesystem and path-related interfaces |
| `http.h` | Basic HTTP client interface |
| `modes.h` | Declarations for the project's named operating modes |
| `protocol.h` | Protocol-related constants and data structures |
| `shell.h` | Command-shell interface declaration |
| `tcp_socket.h` | TCP socket and stream-related interfaces |
| `tuna_socket.h` | Socket and connection-management interfaces |
| `tuna.h` | Top-level class and lifecycle interfaces |
| `tunax1.cpp` | Entry point |
| `trojan_project.pdf` | High-level lifecycle diagram |

## Platform and dependencies

- **Platform indicated by the project:** Windows.
- **Language:** C++.
- The headers reference Windows APIs, Winsock, and `nlohmann/json`.
- The repository does not provide a complete build configuration or all implementation files. Dependency versions, full build steps, and reproducible compilation therefore cannot be guaranteed from this public snapshot alone.

## How to review this repository

1. Browse the header files to understand the declared interfaces and the way the project is divided into components.
2. Read the comments as author-provided documentation, not as proof that each function behaves exactly as described.
3. Consult the PDF for the included high-level lifecycle overview.
4. Do not expect the repository to compile or run as-is; implementation files and private components are intentionally omitted.

## Scope and limitations

- This repository is intentionally incomplete.
- It does not include the private server or the full implementation.
- No claim is made that the interfaces have been independently tested or that the project builds from the published files.
- No operational usage instructions are provided for deploying or controlling malware.

## Third-party notices

The original README attributes `stb_image.h` and `stb_image_write.h` to Sean T. Barrett and links to the [stb repository](https://github.com/nothings/stb). Retain the applicable upstream license and copyright notices when redistributing those files.

## Disclaimer

This repository is published for software-architecture documentation and security-research portfolio purposes. The public files are a partial interface snapshot and should not be interpreted as a complete implementation or as evidence of runtime behavior.
