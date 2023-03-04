# cloudflared-mips
Cloudflared built for MIPS (Open WRT)


I needed to get cloudflare tunnel running in GL-Inet Opal (SF19A28 MIPS LE), so I had to compile this from source.\
\
The code I compiled it with is as follows:
```
docker run --rm -v "/Users/seva/Develop/cloudflare-mips/cloudflared":/usr/src/myapp -w /usr/src/myapp -e GOOS=linux -e GOARCH=mipsle golang:1.19 bash -c "go build -v -mod=vendor github.com/cloudflare/cloudflared/cmd/cloudflared"
```