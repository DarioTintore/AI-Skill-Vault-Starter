---
name: dockerfile
description: Generates an optimized, multi-stage and secure Dockerfile for the project or the selected file. Use to containerize an application.
---

# Dockerfile

Generate a Dockerfile for the project or the selected file ($FILE_NAME). Requirements:

- multi-stage build to reduce the image size
- non-root user for security
- layers ordered to leverage the cache
- suggested .dockerignore
- build and run commands

Briefly explain the choices you made.

```
$SELECTION
```
