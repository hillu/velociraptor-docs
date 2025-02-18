---
title: Linux.Sys.ACPITables
hidden: true
tags: [Client Artifact]
---

Firmware ACPI functional table common metadata and content.

```yaml
name: Linux.Sys.ACPITables
description: Firmware ACPI functional table common metadata and content.
reference:
  - https://osquery.io/schema/3.2.6#acpi_tables
parameters:
  - name: kLinuxACPIPath
    default: /sys/firmware/acpi/tables
sources:
  - precondition: |
      SELECT OS From info() where OS = 'linux'
    query: |
        LET hashes = SELECT Name, Size, hash(path=FullPath) as Hash
                     FROM glob(globs="*", root=kLinuxACPIPath)

        SELECT Name, Size, Hash.MD5, Hash.SHA1, Hash.SHA256 from hashes

```
