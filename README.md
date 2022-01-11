# Repository Style Guide

This guide will break down my recommended style for code repositories.  It can be helpful to include this in the repository README.

_Replace this section with information about why this style guide has been included._

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

- _GitHub Issue_
  > #216 - Link color not changing on hover
- _Branch_
  > 216-hover-link-color

## Issues

Issues are useful to help manage the backlog of feature requests and bug fixes.  Issues can be added by customers, users, or the developer(s) and should be updated frequently.  When a developer begins work on an issue, they should assign it to themselves and ensure that all data and metadata is accurate.

The two most important pieces of metadata are the **assignee** and the **label**:  

- _Assignee_: assigning yourself or another developer to an issue alerts every stakeholder that someone is managing the issue.
  - Multiple developers can be assigned to the same issue if needed.
  - Tagging (@jryantz) can be used to involve other users.
- _Label_: before beginning development, the label should be set to the type of work that is being done.  The following labels are the most used and helpful.
  - _Bug_: any change that resolved a problem experienced by a user.
  - _Documentation_: changes that improve or update documentation in code or the dedicated documentation set.
  - _Enhancement_: any new code that improves or adds functionality.
  - _Tech Debt_: (needs to be created) any changes that remove or fix code that reduces the complexity of the application code base.

Note: the comments section should be used to keep track of crucial decisions made while developing the feature.  

## Releases

Releases provide a simple way to keep track of changes over time.  When a release is created, a tag is created that can be used as a reference to the commit that contains the change.  This reference is a good marker in case a rollback to a previous version is needed.

Releases should only be greated on the main branch.  For example, your main branch could be named any of the following:

- `main`
- `master`
- `release/production`

Always provide good release notes in your release.  These notes provide an easy go-to list of historical changes for both developers and users.

### New Version, Example

- _Tag_: v1.0.0
- _Title_: Release 1.0.0

```
Provide a message outlining the release as a whole.
This can be a short paragraph about the changes and the advantages provided by the changes.

# Enhancements

- List item 1
- List item 2
  - Sub-list item 1
- List item 3

# Bug Fixes

- List item 1
- List item 2
```

### Bug Fix, Example

- _Tag_: v1.0.1
- _Title_: Release 1.0.1

```
# Bug Fixes

- List item 1
- List item 2
```
