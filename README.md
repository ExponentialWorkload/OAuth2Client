# OAuth2Client
Github-Pages based OAuth2 for Discord

## how 2 use

1. Get a URL on some domain (localhost works) like `http://127.0.0.1:8090/oauth-completed`
2. Add a `?` or a `#` to the end
3. Make clients visit https://discord.oauth2.変態.wtf/#redirect_uri=YOUR%20URL%20ENCODED%20URL&client_id=12345678901234567890&scope=identify
4. Replace `YOUR%20URL%20ENCODED%20URL` with the URL Encoded URI (ie, for `http://127.0.0.1:8090/oauth-completed?`, this would be `http%3A%2F%2F127.0.0.1%3A8090%2Foauth-completed%3F`)
5. Once the authentication has been completed, a (usually aprox. 10 minute, less depending on how long the user spent on the auth page) token is provided in the `authorization` URI component/query/thing

***MAKE SURE TO ALLOW `https://discord.oauth2.変態.wtf/flow-completion` ON YOUR APPLICATION AS A REDIRECT URI***

Example final URL: `https://discord.oauth2.変態.wtf/#redirect_uri=https://discord.oauth2.変態.wtf/copy&client_id=12345678901234567890&scope=identify`

## questions
is this secure? not really, i threw it together in like 10 minutes - it's good enough if all you need is say `identify` i guess though
