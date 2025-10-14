---
type: post
author:
  - "[[EwenQuim]]"
link: https://github.com/go-fuego/fuego
created_date: 2025-08-27
updated_date: 2025-08-27
---
## Notes

How to setup the Openapi configration for production
```go
app.OpenAPI.Description().Servers = append(app.OpenAPI.Description().Servers, &openapi3.Server{
		URL:         os.Getenv("PUBLIC_URL"),
		Description: "Production server",
})
```