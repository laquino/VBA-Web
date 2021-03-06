# 4.0.0

- Mac support!
- Custom converters
- Switch to `WinHttpRequest`
- Switch to [VBA-tools/VBA-JSON](https://github.com/VBA-tools/VBA-JSON)

# 3.1.0

- Add `Request.RequestFormat`, `Request.ResponseFormat`, and `Request.Accept` for setting separate request and response formats (e.g. form-urlencoded request with json response)
- Add `LogRequest` and `LogResponse` for better logging detail (enable with `RestHelpers.EnableLogging = True`)
- Allow headers and content-type to be set in authenticator `BeforeExecute`
- __3.1.1__ Fix importing class incorrectly as module bug
- __3.1.2__ Add XML and plain text formats
- __3.1.3__ Fix hard dependency for XML
- __3.1.4__ Fix logging in `PrepareProxyForHttpRequest`

# 3.0.0

- Add `Client.GetJSON` and `Client.PostJSON` helpers to GET and POST JSON without setting up request
- Add `AfterExecute` to `IAuthenticator` (Breaking change, all IAuthenticators must implement this new method)
- __3.0.1__ Add `DigestAuthenticator`, new helpers, and cleanup
- __3.0.2__ Switch timeout to `Long` and remove `RestClientBase` (out of sync with v3)
- __3.0.3__ Update OAuth1, deprecate `IncludeCacheBreaker`, update True/False formatting to lowercase, add LinkedIn example
- __3.0.4__ Fix formatting of parameters with spaces for OAuth1 and add logging
- __3.0.5__ Allow Array and Collection for Body in `Request.AddBody` and `Client.PostJSON`
- __3.0.6__ Convert Empty to `null` for json
- __3.0.7__ Add `install.bat` script for easy installation and upgrade

# 2.3.0

- Add `form-urlencoded` format and helpers
- Combine Body + Parameters and Querystring + Parameters with priority given to Body or Querystring, respectively

# 2.2.0

- Add cookies support with `Request.AddCookie(key, value)` and `Response.Cookies`
- __2.2.1__ Add `Response.Headers` collection of response headers

# 2.1.0

- Add Microsoft Scripting Runtime dependency (for Dictionary support)
- Add `RestClient.SetProxy` for use in proxy environments
- __2.1.1__ Use `Val` for number parsing in locale-dependent settings
- __2.1.2__ Add raw binary `Body` to `RestResponse` for handling files (thanks [@berkus](https://github.com/berkus))
- __2.1.3__ Bugfixes and refactor

# 2.0.0

- Remove JSONLib dependency (merged with RestHelpers)
- Add RestClientBase for future use with extension for single-client applications
- Add build scripts for import/export
- New specs and bugfixes
- __2.0.1__ Handle duplicate keys when parsing json
- __2.0.2__ Add Content-Length header and 408 status code for timeout

# 1.1.0

- Integrate Excel-TDD to fully test Excel-REST library
- Handle timeouts for sync and async requests
- Remove reference dependencies and use CreateObject instead
- Add cachebreaker as querystring param only
- Add Join helpers to resolve double-slash issue between base and resource url
- Only add "?" for querystring if querystring will be created and "?" isn't present
- Only put parameters in body if there are parameters

# 0.2.0

- Add async support
