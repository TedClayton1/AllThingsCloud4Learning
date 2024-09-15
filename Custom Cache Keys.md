
customize the cache keys to omit the protocol from the key explained. Yes, it's possible to customize cache keys to omit the protocol from the key. Here's how to do it for Cloud CDN:

1. Go to the Cloud CDN page in the Google Cloud console
2. Click Add origin
3. Click Select origin
4. Select the origin for which you want to enable CDN
5. Click Configure
6. Clear the checkbox for the Protocol field
7. Click Save
8. Click Add 
    

Custom cache keys allow you to include or omit any combination of the protocol, host, and query string. For example, you can use custom cache keys to:

- Ignore the host part of the request and share cache entries when two hosts resolve to the same IP address
- Ignore the domain but cache the logo when two websites on different domains use the same logo 
    

Changing the cache key configuration may cause a sudden drop in the cache