---
title: Core commands
weight: 68
description: >-
  In this section, you will find more details about commands used through stidn.
---

---

## **Core commands with STDIN**

Here are the JSON used to run Ritchie's core commands through **stdin**.

{{% alert color="warning" %}}

You will have to adapt the variable values of each JSON to perform the desired operations as expected.

{{% /alert %}}

### **General commands**

rit init

```text
echo '{"addCommons":true, "sendMetrics":true, "runType":"local"}' | rit init --stdin
```

rit tutorial

```text
echo '{"tutorial":"enabled"}' | rit tutorial --stdin
```

### **Repo commands**

rit add repo

```text
echo '{"provider":"Github", "name":"repoName", "repoUrl":"https://github.com/ZupIT/ritchie-formulas", "token": null, "priority":1, "tag"="2.2.0"}' | rit add repo --stdin
```

rit update repo

```text
echo '{"name":"repoName", "tag":"2.2.0"}' | rit update repo --stdin
```

rit delete repo

```text
echo '{"name":"repoName"}' | rit delete repo --stdin
```

### **Formula commands**

rit create formula

```text
echo '{"formula":"rit demo create formula", "lang":"shell", "workspacePath":"/users/dennis/home/ritchie-formulas", "formulaPath":"/demo/create/formula"}' | rit create formula --stdin
```

rit build formula

{{% alert color="danger" %}}

Not supported yet

{{% /alert %}}

### **Environment commands**

rit set env

```text
echo '{"env":"envName"}' | rit set env --stdin
```

rit delete env

```text
echo '{"env":"envName"}' | rit delete env --stdin
```

### **Credential commands**

rit set credential

```text
echo '{"service":"provider", "type":"type", "credential": {"username":"credentialUsername","token": "credentialToken"}}' | rit set credential --stdin
```

rit delete credential

```text
echo '{"provider":"provider"}' | rit delete credential --stdin
```

## **Core commands without STDIN**

Some core commands don't need the stdin flag to be executed as they don't have any input parameter to inform:

* **`rit upgrade`**
* **`rit --version`**
* **`rit completion`**
* **`rit list repo`**
* **`rit list credential`**
* **`rit show env`**
