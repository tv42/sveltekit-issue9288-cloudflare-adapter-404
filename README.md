# Bug reproducer

```shell
npm i
npm run build
npx wrangler dev --local
```

```console
curl -v localhost:8787/_app/foo
*   Trying 127.0.0.1:8787...
* Connected to localhost (127.0.0.1) port 8787 (#0)
> GET /_app/foo HTTP/1.1
> Host: localhost:8787
> User-Agent: curl/7.86.0
> Accept: */*
>
* Mark bundle as not supporting multiuse
< HTTP/1.1 500 Internal Server Error
< Content-Type: text/plain; charset=UTF-8
< Date: Thu, 02 Mar 2023 20:37:39 GMT
< Connection: keep-alive
< Keep-Alive: timeout=5
< Transfer-Encoding: chunked
<
KVError: could not find _app/foo/index.html in your content namespace
    at /home/tv/src/others/sveltejs/sveltekit-issueXXX-cloudflare-adapter-404/.svelte-kit/cloudflare-workers-tmp/node_modules/@cloudflare/kv-asset-handler/dist/index.js:247:19
    at Generator.next (<anonymous>)
* Connection #0 to host localhost left intact
```
