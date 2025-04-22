function FindProxyForURL(url, host) {
    // Example: Use proxy server for game-related traffic
    if (shExpMatch(host, "*.mobilelegends.com") || shExpMatch(url, "game.mobilelegends.com")) {
        return "PROXY your-proxy-server-address:port";
    }

    // Default: direct connection for other traffic
    return "DIRECT";
}
