---
title: Go 
description: 'Using Go'
position: 18 
category: 'Languages'
---

Fume supports the use of Go by itself or with the [Gin](https://gin-gonic.com/) and [Fiber](https://gofiber.io) framework


### Fiber

When creating a project with Fiber, you can use [Fume's Adapter](https://github.com/fumeapp/fiber)


```bash
go mod init github.com/you/yourproject
go get github.com/fumeapp/fiber
```

```go
package main

import (
	fume "github.com/fumeapp/fiber"
	"github.com/gofiber/fiber/v2"
)

func main() {
	app := fiber.New()
	app.GET("/", func(c *fiber.Ctx) { c.Status(200).JSON(&fiber.Map{"message": "Hello World"}) })
	fume.Start(app, fume.Options{})
}
```

Here is a [working example repository](https://github.com/fumeapp/fiber-example)

<alert type="info">
Fume recommends fiber
</alert>

### Gin

When creating a project with Gin, you can use [Fume's Adapter](https://github.com/fumeapp/gin)


```bash
go mod init github.com/you/yourproject
go get github.com/fumeapp/gin
```

```go
package main

import (
	fume "github.com/fumeapp/gin"
	"github.com/gin-gonic/gin"
)

func main() {
	routes := gin.New()
	routes.GET("/", func(c *gin.Context) { c.JSON(200, gin.H{"message": "Hello World"}) })
	fume.Start(routes, fume.Options{})
}
```

Here is a [working example repository](https://github.com/fumeapp/gin-example)



### Go by itself

When creating a project you have the option to choose  `Lambda Only` which will create a project with a single lambda function and skip the API Gateway and CloudFront creation.  Using this methodology you may use the [AWS Go Adapter](https://github.com/aws/aws-lambda-go) to create your lambda function.  This is the most basic way to use Go with Fume.


You can get started this way
```bash
go mod init github.com/you/yourproject
go get github.com/aws/aws-lambda-go/lambda
```

Your `main.go` file will look like this:

```go

package main


import (
	"fmt"
	"github.com/aws/aws-lambda-go/lambda"
)

func main() {
    	lambda.Start(Handler)
}

func Handler() {
    fmt.Println("Hello World")
}

```

<alert type="warning">
Fume has no way of invoking your function if you do this - it is up to you to invoke your function.
</alert>

<alert type="info">
No logs will appear in Fume until your function is invoked at least once
</alert>