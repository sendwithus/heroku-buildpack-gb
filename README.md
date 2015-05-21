# heroku-buildpack-gb

A [Heroku Buildpack](https://devcenter.heroku.com/articles/buildpacks) for [Go](https://golang.org/) projects using the [gb build tool](https://github.com/constabulary/gb).

Note this buildpack does *not* use `gb` to compile the app; it only compiles apps matching the gb project definition. 

The app is compiled using the `go build main` command, with the binary being put in `bin/main`.

##### Example project structure

* root/
  * src/
    * main/
      * main.go
  * vendor/
    * github.com/...

##### Example Procfile:
```yaml
web: bin/main -PORT=$PORT
```
