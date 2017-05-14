[![GoDoc](http://godoc.org/github.com/robfig/cron?status.png)](http://godoc.org/github.com/robfig/cron) 
[![Build Status](https://travis-ci.org/robfig/cron.svg?branch=master)](https://travis-ci.org/robfig/cron)

```golang
// 允许调用AddFunc时传额外的参数

c := cron.New()
err := c.AddFunc(item.Spec, func(e *cron.Entry) {
    fmt.Println(e.Param.(string)) // output "hello"
}, "hello")

c.Start()
```