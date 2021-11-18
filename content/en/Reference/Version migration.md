---
title: Version Migration
weight: 95
description: In this section, you will find more information about Ritchie's version migration.
---

## **Ritchie 1.0 and Ritchie 2.0**

Differences between version 1.0 and 2.0

* Ritchie versions **Single** and **Team** are deprecated. _Check the observation below if you still want to use the previous version._ 
* The command tree will be dynamically generated on the added repositories. _So, it won't be necessary to edit formula's repositories tree.json files anymore._ 
* There isn't a cloud storage anymore. _The user can import formulas repositories from Github or Gitlab._ (**`rit add repo`**) __
* Autocomplete support for 2 new shells: **Fish** and **Powershell**. (**`rit completion fish`** | **`rit completion powershell`**) 
* Support to run formula in a container. (**`--docker flag`**) 
* Support to build formulas on Windows OS. 
* New tutorial to the CLI. 
* Structural upgrades.

{{% alert color="danger" %}}

Version 2.0 **doesn't support Vault to share credentials**.
Therefore, if you want to keep using those features, you have to stay on the **1.0 version.**

{{% /alert %}}

## **How can you migrate formulas from V1.0 to V2.0?**

### **Context**

If you use Ritchie 1.0 version and want to upgrade to the 2.0 one, **you have to update your formula's repository structure** to be compatible to the pattern used on the new version.

### **How to migrate?**

**Step 1**: Create new formula repo from scratch using the **`rit create formula`** command.

* Adding the same formulas paths used on the older repository to the new one.

**Step 2:** Export your formulas implementations from the older repository to the new one.

* The structure still uses the same files: **`config.json`** , **`main.*`**, **`formula.*`**.
* Copy these files codes from the old structure to the new one, respecting the new layout.

**Step 3**: Publish the new formula repository on **github** or **gitlab** (also, it can **public** or **private**).

**Step 4**: Generate a release of the formula repository.

**Step 5**: Add the formula repository on Ritchie using the **`rit add repo`** command.

**Step 6**: Share your formula's repository with your team, colleagues or the community.

{{% alert color="info" %}}

If you have any question, feel free to contact our team at **ritchie@zup.com.br** or by opening an issue on the [**ritchie-formulas repository**](https://github.com/ZupIT/ritchie-formulas).

{{% /alert %}}
