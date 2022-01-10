# GitHub Style Guide

This guide will break down the style that I follow when building my repositories.

## Branches

**Release Branches**

These branches should be configured with branch protection, preventing contributors from merging directly into these branches.  Instead contributors should be required to submit a pull request which must be approved by at least one other contributor.

_Examples_:
- `release/production`
- `release/staging`
- `release/development`

**Version Branches**

Version branches do not require branch protection, but could be configured as such if the development team is large.  With branch protection, these branches would prevent merge commits to reduce the risk of code overwrites if local merges are performed incorrectly.  Ideally, the pull request approver would catch any issues and require changes before approving.

_Examples_:
- `1.0.0`
- `1.0.x`
- `1.1.0`
- `2.0.0`

**Feature Branches**

Feature branches are created by contributors to manage their own development.  These branches do not require any protection should be removed once the new feature code has been successfully merged into the version branch.

These branches should always coorespond to a specific Issue with the name representing that connection.

_Example_:

- _GitHub Issue_: #216 - Link color not changing on hover
- _Branch_: 216-hover-link-color

## Issues

Issues are required to help manage your backlog of feature requests and bug fixes.  Issues can be added by customers, users, or developer - but should be updated frequently.  When a developer begins work on an Issue, they should assign themselves and ensure that all data and metadata is accurate.

The two most important pieces of metadata are the **assignee** and the **label**:  

- By assigning yourself or another developer to an issue, this alerts all other developers that someone is managing the issue.  Multiple developers can be assigned to the same issue if needed, and tagging (@jryantz) can be used to involve other users.
- Before beginning development (if not defined during creation), the label should be set to the type of work that is being done.

Note: the comments section should be used to keep track of crucial decisions made while developing the feature.  
