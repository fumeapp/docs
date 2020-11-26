---
title: Kitchen Sinkk
description: 'Setting up a fume account'
position: 30
category: 'Guide'
---

These are `backticks` and these are **asterisks**

Example code snippet with file name

```php{}[App\Models\Project.php]
public function getRepoNameAttribute()
{
    if ($this->repo === null) {
        return null;
    }
    preg_match('/(git@|https:\/\/)git(hub|lab).com[:|\/](.*?)\/(.*?).git/', $this->repo, $matches);
    return "${matches[3]}/${matches[4]}";
}
```

<alert type="info">

Check out an info alert with a `codeblock` and a [link](/themes/docs)!

</alert>

<alert type="warning">

This is an example `Warning` alert

</alert>


## badge
<badge>v1.2+</badge>

## code block
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

> This is a markdown hint using >
