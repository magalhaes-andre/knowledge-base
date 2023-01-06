# What is a Content Repository

A content repository in essence is a storage location for digital content. The structure of this repository is commonly hierarchical and represented as a tree structure, with each node representing a storage location for content.

## JCR (Java Content Repository)

Specification created by the java community to access content repositories in a consistent manner, while being platform and vendor independent. The access to a JCR is provided through the javax.JCR API.

## Difference Between Package and Bundle

Package -> ZIP file containing the content in the form of a file-system serialization ("vault serialization") displaying the content from the repository as an easy use/edit representation of files and folders. Packages can include content and project-related data.

Bundle -> Tightly coupled, dinamically loadable collection of classes, jars, and configuration files that explicitly decalre their external dependencies (if they exist).

## Persistence Manager

The persistence manager saves the repository content to a permanent storage solution. By default CRX saves repository content to the Tar persistence manager. For other options you could consider:

- DB2
- Oracle
- SQL Server
- MySQL