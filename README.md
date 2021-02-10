# Workshop Prototype
A model of how future workshops should be structured to provide maintainability, extensibility, and discoverability

## Purpose

We would like to provide a standard for workshops as we prepare for the launch of .NET 6 in November 2021.  Workshops should have these standard features:

## Modules with Samples and Scripts

Workshops are comprised of modules, where each module teaches a single concept.  Each module is made of the following:

- A 'before state' that provides a starting point for students to begin the module
- A 'completed state' that demonstrates how the module should be successfully completed
- A demo-script for instructors or students who wish to learn the workshop on their own.

### Samples Code for each Module

Sample code shall be provided so that it's available to run on as many operating systems as possible.  An isolated solution file and projects should be provided for both the before and completed states of the sample code.

### Demo Scripts

Scripts should be provided in markdown format, named README.md and linked so that one can navigate from one module to the next.  This will allow the script to be viewable on GitHub and can be republished on a workshop hosting website linked to www.dot.net  

### Build Scripts

All workshops will carry GitHub actions that build and potentially execute unit tests to verify that demos all continue to function.  All samples should be built for every pull-request and commit to the `main` branch to ensure the quality and completeness of the samples provided.

### Standard Folder Structure

Workshops have this folder structure:

```
/
/.devcontainer/.devcontainer.json 
/.github/workflows/workshop.yml 
/README.md 
/modules
/modules/module-XX
/modules/module-XX/README.md 
/modules/module-XX/begin 
/modules/module-XX/complete 
/modules/module-XX/img 
/tests
```