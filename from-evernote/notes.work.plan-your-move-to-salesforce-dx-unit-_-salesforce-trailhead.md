---
id: 8ZbH0MmKNifgwCSvOSrGC
title: Plan Your Move to Salesforce Dx Unit _ Salesforce Trailhead
desc: ''
updated: 1645225706341
created: 1645225706341
stub: false
isDir: false
---
My Template
---

_Created at 2018-06-08._
_Last updated at 2018-06-08._
_Source URL: [](https://trailhead.salesforce.com/trails/sfdx_get_started/modules/sfdx_dev_model/units/sfdx_dev_model_evolve_to_dx)._



Tagged: 
```
salesforce
```


---

# Plan Your Move to Salesforce DX Unit | Salesforce Trailhead


# Plan Your Move to Salesforce DX

## Learning Objectives

After completing this unit, you’ll be able to:

*   Identify use cases where you can shift to a modular (artifact-based) approach.
*   Identify a scenario that doesn't lend itself to artifact-based development.

## Next Stop: Planning Your Transition to Salesforce DX

Now that you understand how to use Salesforce DX and recognize its value, you’re interested in moving forward with it. So how do you begin to use it? That depends on the complexity and maturity of your production org and the associated development processes. Here are some suggestions to help you get started.

## Look for Ways to Unwind the Org into Artifacts

Evaluate all aspects of your development process to look for possible ways to shift to the modular artifact-based approach. Look for distinct applications in the production org that are separate from everything else. Do you have distinct teams that build and maintain these applications? If so, you can isolate those applications into their own artifacts. [AppExchange](https://appexchange.salesforce.com/) has a lot of great examples of standalone apps that follow this idea of isolating a set of source and metadata into a single artifact.

In some cases, you won’t have a distinct application that can be split into an artifact, but you will find distinct parts of your org that have been worked on over a period of time. For instance, extensions to one of your core apps could be released as artifacts. You can isolate all of the extensions you make in customizing your company’s sales process into a single artifact. If you can isolate the metadata that is specific to these parts, you can use that to develop an artifact.

You can also look for teams who already, or would like to, build and deliver separately from everyone else. Some teams may be looking for opportunities to be more agile and flexible—they want to separate their changes from the larger change management process in their production org. These teams can isolate their metadata and store them in their own artifact.

## Look Out for Shared Metadata

Along the way, ensure that you evaluate all potential artifacts for shared metadata components. You don’t want to inadvertently isolate shared metadata to an artifact owned by a specific team or application. If the metadata component is shared, we recommend that you organize those shared components into a single base artifact. In this way, you can ensure that all artifacts can reference the components in the shared artifact. (Remember, metadata components can only live in one artifact at a time.)

## Retrieve the Metadata Source

Once you’ve identified potential artifacts, you’ll use the Metadata API to retrieve the source related to your artifact. See the [App Development with Salesforce DX](https://trailhead.salesforce.com/modules/sfdx_app_dev) module to walk through how you’d use the Salesforce CLI and your testing org to create a package.xml that identifies the components of the artifact. Once you’ve extracted the source, create a VCS repository for each artifact. From there you can continue the separation process by building release cycles specific to those applications.

## Rome Wasn’t Built in a Day

Are you a developer who has only worked in the org-based development model, or did you start your career as an admin? Then the Salesforce DX source-driven model is a perfect opportunity to embrace a more agile and flexible development process.

If your organization has a mature or complex org, the shift to the source-driven model needs to occur over time. Your production org is your most prized possession, so plan your transition thoughtfully. Use the guidance in this unit to identify parts of your org that you can shift to Salesforce DX. Shift one artifact at a time and continue to evaluate and improve your process.

Now that you know more about the Salesforce DX development model, it’s time to get your fingernails dirty by trying it out.

