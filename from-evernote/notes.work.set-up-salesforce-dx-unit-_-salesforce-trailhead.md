---
id: lCoerIjunfb9c2SqfOWa2
title: Set up Salesforce Dx Unit _ Salesforce Trailhead
desc: ''
updated: 1645225706359
created: 1645225706359
stub: false
isDir: false
---
My Template
---

_Created at 2018-06-12._
_Last updated at 2018-06-12._
_Source URL: [](https://trailhead.salesforce.com/trails/sfdx_get_started/modules/sfdx_app_dev/units/sfdx_app_dev_setup_dx)._



Tagged: 
```
salesforce
```


---

# Set Up Salesforce DX Unit | Salesforce Trailhead


# Set Up Salesforce DX

![unknown_filename.2.png](/assets/unknown_filename-gGnQ0t52KZ20.png)

**Attention, Trailblazer!**

Salesforce has two different desktop user interfaces: Lightning Experience and Salesforce Classic. This module is designed for **Lightning Experience**.

You can learn about [switching between interfaces](https://help.salesforce.com/articleView?id=lex_switching_uis.htm&language=en_US), [enabling Lightning Experience](https://help.salesforce.com/articleView?id=lex_enable_intro.htm&language=en_US), and more in the [Lightning Experience Basics](https://trailhead.salesforce.com/module/lex_migration_introduction) module here on Trailhead.

## Learning Objectives

After completing this unit, you’ll be able to:

*   Describe how the model for traditional monolithic org development differs from modular artifact development.
*   Describe the key characteristics of an artifact.

## Get Started with Salesforce DX

Salesforce DX is a new set of tools that streamlines the entire development life cycle. It improves team development and collaboration, facilitates automated testing and continuous integration, and makes the release cycle more efficient and agile.

But Salesforce DX is so much more than just a new set of tools! It’s a new development paradigm that shifts the source of truth from the org to your version control system (VCS). It shifts your development focus from org-based development to artifacts-based development. If you want to learn how to migrate your existing dev processes to Salesforce DX, head over to the [Salesforce DX Development Model](https://trailhead.salesforce.com/modules/sfdx_dev_model) module.

But enough with the chit-chat. Are you ready to start getting hands-on with Salesforce DX? Let’s get started setting up your environment and introducing you to some new and some familiar tools.

## What’s a Scratch Org?

Much of the setup you do for Salesforce DX enables you to use a new type of org called a scratch org. A scratch org is a dedicated, configurable, and short-term Salesforce environment that you can quickly spin up when starting a new project, a new feature branch, or a feature test.

Although scratch orgs are meant to be disposable, the scratch org configuration files contain the real brawn. Through the configuration file, you can configure the scratch org with different Salesforce editions and with just the features and preferences you want. And you can share the scratch org configuration file with other team members. That way, you all have the same basic org in which to do your development.

So far, so good? Read on...

## Sign Up for a Developer Hub Trial Org

A Developer Hub (Dev Hub) provides you and your team with the ability to create and manage scratch orgs. Scratch orgs are temporary Salesforce environments where you do the bulk of your development work in this new source-driven development paradigm.

To get started with Salesforce DX, you choose an org to function as your Dev Hub. While you can enable Dev Hub in any paid org, it’s always best to practice somewhere other than production. Instead, go ahead and sign up for a [Dev Hub trial org](https://developer.salesforce.com/promotions/orgs/dx-signup) to use with this module. It already has Dev Hub enabled so you can skip ahead to the good stuff. Trial Dev Hub orgs expire after 30 days, but that’s enough time for you to test things, complete the work in this module, and earn your badge!

You can also make any paid org your Dev Hub and grant access to developers. Get the details in the [Salesforce DX Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.214.0.sfdx_setup.meta/sfdx_setup).

Now that you have a Dev Hub org, let’s set up the rest of your Salesforce DX tools.

## Install the Command Line Interface (CLI)

Use the Salesforce CLI to control the full application life cycle of your apps. You can easily create environments for development and testing, synchronize source code between your orgs and VCS, and execute tests.

![unknown_filename.png](/assets/unknown_filename-UbHoeKqkkAUC.png)

See the [Salesforce DX Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.214.0.sfdx_setup.meta/sfdx_setup) for complete installation instructions.

1.  Install the CLI.
    
    | Operating System | Link to Installer |
    | --- | --- |
    | macOS | <https://sfdc.co/sfdx_cli_osx> |
    | Windows 32-bit | <https://sfdc.co/sfdx_cli_win> |
    | Windows 64-bit | <https://sfdc.co/sfdx_cli_win64> |
    | Debian/Ubuntu 64 | <https://sfdc.co/sfdx_cli_linux><br><br>Download the archive from one of the URLs in the manifest, extract the archive, then run the ./install script. |
    | Debian/Ubuntu x86 | <https://sfdc.co/sfdx_cli_linux_x86><br><br>Download the archive from one of the URLs in the manifest, extract the archive, then run the ./install script. |
    
    Let’s make sure the CLI is properly installed and you know how to access online help for the commands.
    
2.  In a command window, enter sfdx.
    
    You’ll see something like this:
    
        Usage sfdx COMMAND commandspecificoptions
        Help topics type "sfdx help TOPIC"  more details
        sfdx force # tools  the salesforce developer
        sfdx plugins # manage plugins
        sfdx update # update sfdxcli
        
    

![unknown_filename.png](/assets/unknown_filename-UbHoeKqkkAUC.png)

If you don’t see this type of response, enter sfdx update to ensure that you have the Salesforce DX plug-in and the latest bits.

Here are some other helpful commands to get you started:

| Command | What You See |
| --- | --- |
| sfdx force --help | All the available topics |
| sfdx force:doc:commands:list | All available commands |

OK, you’re well on your way. Now let’s continue installing the rest of the Salesforce DX tooling.

## Log In to the Dev Hub

To get started, log in to the Dev Hub using the CLI, so you’re authorized to create scratch orgs. You can use sfdx force:auth:web:login to log in to various orgs, and we’ve provided some options to help you manage those orgs.

You can display help for any command. Help provides information on what the command does, describes each parameter, and lists the short and long versions of the parameters. Here's how to display help for the first command you'll run.

    sfdx forceauthweblogin h
    sfdx forceauthweblogin help

1.  To authorize the Dev Hub, use the web login flow:
    
        sfdx forceauthweblogin d a DevHub
    
    Adding the \-d flag sets this org as the default Developer Hub. Use the \-a to set an alias for the org (something catchy like DevHub). An alias is much easier to remember than the unique Dev Hub username.
    
    ![unknown_filename.1.png](/assets/unknown_filename-yz1nKqX71fBH.png)
    
    #### Important
    
    Only indicate the \-d flag for your Dev Hub. If you use it with a different org, you won’t be able to create scratch orgs until you correctly identify the Dev Hub using the config:set command.
    
2.  Log in with your credentials.
    
    Once successful, the CLI securely stores the token along with the alias for the org, in this example, DevHub. You can close the Dev Hub org at any time.
    

You can close the Dev Hub and still create scratch orgs. However, if you want to open the Dev Hub org to look at active scratch orgs or your namespace registry, the alias comes in quite handy:

    sfdx forceorgopen u DevHub

## A Bit More on Org Management

### Log In to Sandboxes

It’s likely you have many orgs, including sandboxes and your production org. With the CLI, you can also log in to them using these commands. When you log in to an org using the CLI, you add that org to the list of orgs that the CLI can work with in the future. If you create an alias for the sandbox (\-a option), you can reference it by this alias instead of its long and often unintuitive username.

For example:

    sfdx forceauthweblogin r httpstestsalesforcecom a FullSandbox
    sfdx forceauthweblogin r httpstestsalesforcecom a DevSandbox

![unknown_filename.1.png](/assets/unknown_filename-yz1nKqX71fBH.png)

#### Important

Remember, don’t use the \-d flag. If you do, the CLI thinks the org is your Developer Hub, and then you’ll see an error when you try to create a scratch org.

### The Power of Aliasing

As you might imagine, aliasing is a powerful way to manage and track your orgs, and we consider it a best practice. Why? Let’s look at scratch org usernames as an example. A scratch org username looks something like scratchorg1484322002940@acme.com. Not easy to remember. So when you issue a command that requires the org username, using an alias for the org that you can remember can speed things up.

    sfdx forceorgopen u FullSandbox
    sfdx forceorgopen u MyScratchOrg
    sfdx forcelimitsapidisplay u DevSandbox

### View All Orgs

At any point, you can run the command sfdx force:org:list to see all the orgs you’ve logged in to. Adding the \--verbose option provides you even more info.

Now you’re really ready to get going—let’s go build a new app with Salesforce DX.

+100 points

Use Dev Hub to:

Manage sandbox and production orgs through the command line.
Create and manage your scratch orgs.
Move configurations from your sandbox to your scratch org.
Create a scratch org for another team member.

How do you list all available CLI commands?

sfdx force:commands:view
sfdx force:list:help
sfdx force:doc:commands:list
sfdx force:doc:commands:view
sfdx force:commands:doc:display

Second attempt earns 50 points. Three or more earns 25 points.

