---
id: IOJGKCZl4iJ9OmVT2pBFP
title: Understand Source Driven Development Unit _ Salesforce Trailhead
desc: ''
updated: 1645225706366
created: 1645225706366
stub: false
isDir: false
---
My Template
---

_Created at 2018-06-08._
_Last updated at 2018-06-08._
_Source URL: [](https://trailhead.salesforce.com/trails/sfdx_get_started/modules/sfdx_dev_model/units/sfdx_dev_model_sdd)._



Tagged: 
```
salesforce
```


---

# Understand Source-Driven Development Unit | Salesforce Trailhead


# Understand Source-Driven Development

## Learning Objectives

After completing this unit, you’ll be able to:

*   Describe the purpose of a Salesforce DX project.
*   Describe how Salesforce DX helps you manage change tracking.
*   Explain the role of scratch orgs in the development process.

## Now the Fun Begins

As we learned in the previous unit, with Salesforce DX you decide which tools to use. You can use your favorite text editor in conjunction with the Salesforce CLI or Salesforce Extensions for VS Code. You select which VCS you want to use. If using Salesforce Extensions for VS Code, we offer several extensions to facilitate developing with Salesforce DX.

For source-driven development, your source is organized into artifacts based on a group of features or customizations you want to deliver together. The Salesforce DX project reflects this artifact-based approach to organizing your source.

## What Is a Salesforce DX Project?

A Salesforce DX project is a local directory structure of your artifact source and Salesforce DX metadata that lets you develop and test with Salesforce DX tooling.

It contains configuration files for creating scratch orgs. It can contain data to be loaded into orgs for development or testing. It should also contain tests that you rely on to validate your artifact.

When you use the CLI to create a new Salesforce DX project, it creates the project directory structure for you. When creating a project from scratch, many things are created for you. We create a base project configuration file. We create sample scratch definition files and directories for your tests and sample data sets. We also create a default “package” directory for your artifact source.

Remember, an artifact is a group of related code and customizations. You can test an artifact independently from other components in your org. An artifact can be released independently as well. The metadata components within an artifact can live in only one artifact at a time.

At a minimum, the project manages the source for one artifact. That being said, if multiple artifacts get built and released together, you can organize these artifacts into a single SFDX project. Each of your artifacts aligns to a package directory defined in the project configuration file.

## How Scratch Orgs Rock the Development Process

Scratch orgs, built from your source and metadata, make it easy for you to build your app consistently over and over again. You only work with the source and metadata for a specific project. There’s no need to copy over things you don’t need (and frankly, we don’t recommend it). And because scratch orgs are temporary Salesforce environments, you can quickly spin up a new scratch org for each artifact or development project.

Once your VCS is set up, and your source is organized into artifacts, you’re ready to start a new development project. Open up your favorite IDE or text editor, then add or modify your source code. When you’re ready to see your changes in an org, you can create a scratch org.

After you create a scratch org, you still have some setup tasks to complete. You need to push all source from the project to the scratch org, set up permissions, and create or load any test data that’s required to use your artifact.

While the IDE or text editor is available for programmatic (code-based) development, you can use the scratch org for declarative (point-and-click) development, just like you did in your sandbox or production org in the org-based development model. What’s different in the source-driven model is that you’ll synchronize any development you did in the scratch org with your local project. This lets you commit changes made in the Setup pages alongside changes made in your local IDE.

Before you commit to your version control system, be sure to run tests. You can either use the same scratch org to run tests, or spin up another specifically for testing before you commit your source. This same pattern of spinning up scratch orgs for testing will become a key part of an automated continuous integration system.

## Keep Your Project and Scratch Org in Sync

A key feature of Salesforce DX is that you can easily keep your project and scratch org in sync. So you can put away those sticky notes! You no longer have to jot down what you changed in your local file system, IDE, or editor, or what you changed in your org.

Salesforce DX keeps track of any change you make locally in the project and any changes you have made in your scratch org.

Before you push source metadata changes to the scratch org, or pull changes from the scratch org to your local project, you can view a list changes you’ve made. That’s the power of the Salesforce CLI in action.

    $ sfdx forcesourcestatus
    STATE                     FULL NAME    TYPE        PROJECT PATH
    ─────                     ──────────   ──────────  ─────────────────────────────────
    Local Deleted             MyClass      ApexClass   MyClassclsmetaxml
    Local Deleted             MyClass      ApexClass   MyClassclsxml
    Local Add                 OtherClass   ApexClass   OtherClassclsmetaxml
    Local Add                 OtherClass   ApexClass   OtherClassclsxml
    Local Add                 Event        QuickAction EventquickActionmetaxml
    Remote Deleted            TempClass    ApexClass   TempClassclsmetaxml
    Remote Deleted            TempClass    ApexClass   TempClassclsxml
    Remote Changed Conflict NewClass     ApexClass   NewClassclsmetaxml
    Remote Changed Conflict NewClass     ApexClass   NewClassclsxml

Within a production org, source files can be really big, with a footprint larger than Sasquatch’s. Think about all the custom objects, custom labels, and static resources that comprise an org, to name a few.

Salesforce DX solves this problem by providing a new source shape that breaks down these large source files to make them more digestible and easier to manage with a version control system. For example, Salesforce DX transforms custom objects and custom object translations into multiple files and directories. This source structure makes it much easier to find what you want to change or update. Smaller files in source control mean fewer merge conflicts during team development. Just say bye-bye to messy merges!

Once you’re done developing, always commit your changes back into the VCS repo. Now you’re ready to test, build, and release with Salesforce DX.

