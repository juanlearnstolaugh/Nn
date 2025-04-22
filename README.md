function FindProxyForURL(url, host) {
    // Example: Route gaming servers traffic through a proxy
    if (shExpMatch(host, "*.mobilelegends.com") || shExpMatch(url, "*.mobilelegends.com")) {
        return "PROXY your-optimized-proxy-server.com:PORT";
    }
    
    // Default: direct connection for other services
    return "DIRECT";
}
