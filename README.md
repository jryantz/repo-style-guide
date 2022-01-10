# GitHub Style Guide

This guide will break down the style that I follow when building my repositories.

## Branches

**Release Branches**

These branches should be configured with branch protection, preventing contributors from merging directly into these branches.  Instead contributors should be required to submit a pull request which must be approved by at least one other contributor.

Examples:
`release/production`
`release/staging`
`release/development`

**Version Branches**

Version branches do not require branch protection, but could be configured as such if the development team is large.  With branch protection, these branches would prevent merge commits to reduce the risk of code overwrites if local merges are performed incorrectly.  Ideally, the pull request approver would catch any issues and require changes before approving.

Examples:
`1.0.0`
`1.0.x`
`1.1.0`
`2.0.0`

**Feature Branches**

Feature branches are created by contributors to manage their own development.  These branches do not require any protection should be removed once the new feature code has been successfully merged into the version branch.

These branches should always coorespond to a specific Issue with the name representing that connection.

Examples:

GitHub Issue: #216 - Link color not changing on hover

Branch: 216-hover-link-color
