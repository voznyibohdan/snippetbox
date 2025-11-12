Listing upgradable packages:

```bash
go list -u -f '{{if (and (not (or .Main .Indirect)) .Update)}}{{.Path}}: {{.Version}} -> {{.Update.Version}}{{end}}' -m all
```

<br/>

Generate local tls certificate: https://github.com/FiloSottile/mkcert
```bash
go run /opt/homebrew/Cellar/go/1.25.3/libexec/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost   
```