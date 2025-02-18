---
title: Server.Internal.ToolDependencies
hidden: true
tags: [Client Artifact]
---

An internal artifact that defines some tool
depenencies. Velociraptor releases for offline collector


```yaml
name: Server.Internal.ToolDependencies
description: |
  An internal artifact that defines some tool
  depenencies. Velociraptor releases for offline collector

tools:
  - name: VelociraptorWindows
    github_project: Velocidex/velociraptor
    github_asset_regex: windows-amd64.exe
    serve_locally: true

  - name: VelociraptorWindows_x86
    github_project: Velocidex/velociraptor
    github_asset_regex: windows-386.exe
    serve_locally: true

  - name: VelociraptorLinux
    github_project: Velocidex/velociraptor
    github_asset_regex: linux-amd64-musl
    serve_locally: true

  - name: VelociraptorDarwin
    github_project: Velocidex/velociraptor
    github_asset_regex: darwin-amd64
    serve_locally: true

  - name: VelociraptorWindowsMSI
    github_project: Velocidex/velociraptor
    github_asset_regex: windows-amd64.msi
    serve_locally: true

  - name: VelociraptorWindows_x86MSI
    github_project: Velocidex/velociraptor
    github_asset_regex: windows-386.msi
    serve_locally: true

```
