# Golang

* [The Go Programming Language](https://golang.org/)
* Extension: [Go](https://marketplace.visualstudio.com/items?itemName=lukehoban.Go)
* Debugger: [delve](https://github.com/derekparker/delve)

## Instraction

### MacOS

1. `brew install golang`
2. `brew install delve`
3. install extension "Go"
4. `F1`->`Go: Install/Update Tools`

### Windows


### Linux

## unit test

1. install golang and add go/bin to PATH
2. `go get github.com/delveparker/delve`
3. install extension "Go"
4. `F1`->`Go: Install/Update Tools`

source : [module_test.go](module_test.go)

### inline

![inline unit test](inline_unit_test.png)

### launch json

menu:`GoLaunch test function`

```
{
	"version": "0.2.0",
	"configurations": [
		{
			"name": "Launch test function",
			"type": "go",
			"request": "launch",
			"mode": "test",
			"program": "${workspaceRoot}",
			"args": [
				"-test.run",
				// test function name
				// can use reguler expression
				// NOT include "Test"
				"BubbleSort"
			]
		}
}
```

## executable file debug

souce: [cmd/bubbleSorter/main.go](cmd/bubbleSorter/main.go)