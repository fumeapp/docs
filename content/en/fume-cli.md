---
title: Fume CLI 
description: 'Setting up the Fume CLI'
position: 5
category: 'Guide'
---

### Install the CLI globally
Install the CLI using `yarn` or `npm` 

<code-group>
  <code-block label="Yarn" active>

  ```bash
  yarn global add fume-cli
  ```

  </code-block>
  <code-block label="NPM">

  ```bash
  npm install -g fume-cli
  ```

  </code-block>
</code-group>

### Connect your workstation to Fume

```bash
fume login
```

* Please make sure you're authenticated with fume on this machine.
* You will be prompted to open your default browser to approve your machine.

### Connect Fume to your projects codebase

* CD to the root folder of your project, or where `nuxt.config.js` resides.

```bash
cd ~/my-project
fume config
```

* The CLI will then ask you to choose a project, then create a `fume.yml`
  * Feel free to add this file to your codebase

