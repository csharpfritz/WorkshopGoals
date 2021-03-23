# Workshop Goals
A model of how future workshops should be structured to provide maintainability, extensibility, and discoverability

## Purpose

We would like to provide a standard for workshops as we prepare for the launch of .NET 6 in November 2021. All workshops should be MIT licensed and encourage contributions.  Workshops should have these standard features:

### Setup Instructions

Detailed instructions to help get development environments to the expected beginning state should be provided.  Any links to Microsoft properties should be embedded with aka.ms links.  This should be delivered in a SETUP.md file and any custom required assets should be embedded in an optional `/setup` folder.  Example:  emulators and hardware configuration for mobile application workshops

### Finished Application

For workshops that build up a single application or system, the finished product should be made available in a `/src` folder

### Modules with Samples and Scripts

Workshops are comprised of modules, where each module teaches a single concept.  Each module is made of the following:

- An optional 'before state' that provides a starting point for students to begin the module
- A 'completed state' that demonstrates how the module should be successfully completed
- A demo-script for instructors or students who wish to learn the workshop on their own.

#### Sample Code for each Module

Sample code shall be provided so that it's available to run on as many operating systems as possible.  An isolated solution file and projects should be provided for the completed states of the sample code.  A begin state of the sample is only required when the module starts with a state that is not the results of `Setup` or the previous module.

#### Demo Scripts for each Module

Scripts should be provided for each module in markdown format, named README.md, and linked to each other so that one can navigate from one module to the next.  This will allow the script to be viewable on GitHub and can be republished on a workshop hosting website linked to www.dot.net  

#### Build Scripts

All workshops will carry GitHub actions that build and potentially execute unit tests to verify that demos all continue to function.  All samples should be built for every pull-request and commit to the `main` branch to ensure the quality and completeness of the samples provided.

#### Speaker Notes

A `notes.md` file should be provided with an outline of the lesson in each module folder and any notes to be passed along to a speaker presenting the workshop. 

#### Additional documentation

Workshops may have a `/docs` folder that contains Powerpoint slides, images, and additional supporting documentation for the instructor. 

### Standard Folder Structure

Workshops have this folder structure:

```
/
/.devcontainer/.devcontainer.json 
/.github/workflows/workshop.yml 
/LICENSE
/speaker-notes.md
/README.md
/VIDEO.md
/docs
/migration
/modules
/modules/module-XX
/modules/module-XX/README.md 
/modules/module-XX/notes.md 
/modules/module-XX/begin 
/modules/module-XX/complete 
/modules/module-XX/img 
/setup
/setup/README.md
/src
/tests
```

### Extensibility of the workshop

It is a goal of these workshops that they last a long time and are upgraded between versions of .NET and tools.  To help facilitate this, we will encourage an extensible model for workshops so that additional parties can write modules that can be added on to the base workshop.

Tagging will be used on the workshop to create 'workshop releases' that indicate the version of .NET and corresponding tools that workshop supports.  In this way, we can also create workshop modules that addresses migrating from one version of .NET and tools to the next version.  These migration modules should not address migrating across more than 1 version of tools at a time.

### External Contributions

TBD

### Videos

The `VIDEOS.md` file shall be created to reference links to any presentations of the workshop that are recorded and made available on a streaming platform.

## Template Workshop

To help get workshop authors started, we are providing a workshop template repository that can be used to organize and start building your workshop with good practices already configured.
