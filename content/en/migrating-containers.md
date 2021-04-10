---
title: Migrating to Containers
description: 'Optional steps to migrate your existing projects to the new container system'
position: 21
category: 'Migrations'
---

There are two major ways to upgrade to Container support.

## Option 1 - Delete everything
> more steps, no AWS interaction
1. Make sure you have upgraded to the latest version of the CLI

 <code-group>
   <code-block label="Yarn" active>

  ```bash
  yarn global upgrade fume-cli
  ```

  </code-block>
  <code-block label="NPM">

  ```bash
  npm update -g fume-cli
  ```

  </code-block>
</code-group>

2. Delete all existing environments
    - You may need to delete any mapped domains
3. Delete all existing projects
4. Remove and re-add your IAM account connected to your team.
5. Re-create your projects, environments, and then deploy!

## Option 2 - Manually update your AWS role
> fewer steps, requires AWS interaction
1. Make sure you have upgraded to the latest version of the CLI
   
 <code-group>
   <code-block label="Yarn" active>

  ```bash
  yarn global upgrade fume-cli
  ```

  </code-block>
  <code-block label="NPM">

  ```bash
  npm update -g fume-cli
  ```

  </code-block>
</code-group>

2. Delete all existing environments
   - You may need to delete any mapped domains
3. Go to the IAM section of your AWS account and navigate to the `fume-role`    
4. Edit the policy (JSON), copy and paste the updated role [here](/fume-role) 
5. Save the policy (you will notice we now ask for ECR permissions)
6. Re-create your environments and deploy!
