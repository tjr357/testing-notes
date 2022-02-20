---
id: myfIoUhObYkRcgzt5GnC5
title: 'Learn How to Test, Build, and Release with Salesforce Dx Unit _'
desc: ''
updated: 1645225706337
created: 1645225706337
stub: false
isDir: false
---
My Template
---

_Created at 2018-06-08._
_Last updated at 2018-06-08._
_Source URL: [](https://trailhead.salesforce.com/trails/sfdx_get_started/modules/sfdx_dev_model/units/sfdx_dev_model_release)._




---

# Learn How to Test, Build, and Release with Salesforce DX Unit |


# Learn How to Test, Build, and Release with Salesforce DX

## Learning Objectives

After completing this unit, you’ll be able to:

## Testing and Continuous Integration Using Scratch Orgs

How you test, build, and release with Salesforce DX is a shift from the current application life cycle.

If you’re currently using the change set development model, you move org changes (diffs) between development and test environments until those changes are released to your production org. But at the end of the day, the “source of truth” is the production org. Even if you track changes externally in a version control system, you know for sure that everything resides in your org.

But now you have options! In the package development model, the new and improved source of truth is your version control system. You use Salesforce DX projects to organize your source into package directories. Your end goal is to create packages using those directories that are versionable, easy to maintain, update, install, and upgrade.

![unknown_filename.png](/assets/unknown_filename-DABk27cdwOAL.png)

When you’re ready to perform manual/exploratory testing of your development work, create and push your metadata into a separate scratch org designated for that purpose (1). You never pull anything from that org, as it’s only being used for testing/validation.

Continuous integration (CI) is about automating consistent test runs against every set of changes merged to your application (2). This ensures application quality before any corrupt change can get into your source repository.

Scratch orgs can be easily integrated into a CI process. The CLI can create scratch orgs, so scripting them into a CI flow is a piece of cake. You can populate the org with the appropriate version of the source repository and run tests on the specific change.

Unlike developer sandboxes, scratch orgs can be created throughout the day as opposed to a single refresh per day. You can delete a scratch org and create a new one quickly when you need to. You can have multiple scratch orgs for different purposes. Scratch orgs give you a ton of flexibility with very limited overhead.

Once you’re ready for testing, you create a packages. Instead of using change sets to move changes between environments, you create and install package versions (3) in each testing environment. Once you complete testing, you install a package version in your production org.

