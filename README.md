### colly
---
https://github.com/gocolly/colly

```go
func main() {
  c := colly.NewCollector()
  
  c.OnHTML("a[href]", func(e *colly.HTMLElement) {
    e.Request.Visit(e.Attr("href"))
  })
  
  c.OnRequest(func(r *colly.Request) {
    fmt.Println("Visiting", r.URL)
  })
  
  c.Visit("http://go-colly.org/")
}
```

```
go get -u github.com/gocolly/colly/...
```

```
```


