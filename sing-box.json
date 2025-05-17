{
    "dns":{
        "servers":[
            {"tag":"cloudflare","type":"https","server":"1.1.1.1","detour":"Proxy"},
            {"tag":"ali","type":"https","server":"223.5.5.5"},
            {"tag":"remote_fakeip","address":"fakeip"}
        ],
        "rules":[
            {"outbound":"any","server":"ali"},
            {"clash_mode":"Direct","action":"route","server":"ali"},
            {"clash_mode":"Proxy","action":"route","server":"remote_fakeip"},
            {"query_type": "HTTPS","action": "reject"},
            {"query_type":["A","AAAA"],"action":"route","server":"remote_fakeip","rewrite_ttl":1},
            {"rule_set":["ChinaDomain","Apple"],"action":"route","server":"ali"}
        ],
        "final":"cloudflare",
        "fakeip": {"enabled": true,"inet4_range": "10.19.0.0/16","inet6_range": "fc00::/18"},
        "independent_cache":true,
        "strategy":"prefer_ipv4"
    },
    "outbounds":[
        {"tag":"direct","type":"direct"},
        {"tag":"Proxy","type":"selector","outbounds":["🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"direct","interrupt_exist_connections":true},
        {"tag":"AI","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Google","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Microsoft","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Twitter","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Telegram","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Emby","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Game","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Spotify","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"ProxyMedia","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan"],"default":"Proxy","interrupt_exist_connections":true},
        {"tag":"Final","type":"selector","outbounds":["Proxy","🇭🇰 HongKong","🇺🇸 United States","🇸🇬 Singapore","🇯🇵 Japan","🇨🇳 Taiwan","direct"],"default":"Proxy","interrupt_exist_connections":true},

        {"tag":"🇭🇰 HongKong","type":"urltest","outbounds":[],"url":"http://1.1.1.1/generate_204","interval":"10m","tolerance":0,"interrupt_exist_connections":false},
        {"tag":"🇺🇸 United States","type":"urltest","outbounds":[],"url":"http://1.1.1.1/generate_204","interval":"10m","tolerance":0,"interrupt_exist_connections":false},
        {"tag":"🇸🇬 Singapore","type":"urltest","outbounds":[],"url":"http://1.1.1.1/generate_204","interval":"10m","tolerance":0,"interrupt_exist_connections":false},
        {"tag":"🇯🇵 Japan","type":"urltest","outbounds":[],"url":"http://1.1.1.1/generate_204","interval":"10m","tolerance":0,"interrupt_exist_connections":false},
        {"tag":"🇨🇳 Taiwan","type":"urltest","outbounds":[],"url":"http://1.1.1.1/generate_204","interval":"10m","tolerance":0,"interrupt_exist_connections":false}
    ],
    "route":{
        "default_domain_resolver":{"server":"ali","rewrite_ttl":3600,"client_subnet":"210.21.4.130"},
        "rule_set":[
            {"tag":"Ads","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Ads_SukkaW.srs","download_detour":"direct"},
            {"tag":"Telegram","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Telegram.srs","download_detour":"direct"},
            {"tag":"YouTube","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/YouTube.srs","download_detour":"direct"},
            {"tag":"Google","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Google.srs","download_detour":"direct"},
            {"tag":"Microsoft","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Microsoft.srs","download_detour":"direct"},
            {"tag":"OneDrive","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/OneDrive.srs","download_detour":"direct"},
            {"tag":"Github","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Github.srs","download_detour":"direct"},
            {"tag":"Twitter","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Twitter.srs","download_detour":"direct"},
            {"tag":"Apple","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Apple.srs","download_detour":"direct"},
            {"tag":"AppleProxy","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/AppleProxy.srs","download_detour":"direct"},
            {"tag":"AI","type":"remote","format":"binary","url":"https://git.repcz.link/raw.githubusercontent.com/MetaCubeX/meta-rules-dat/sing/geo/geosite/category-ai-chat-!cn.srs","download_detour":"direct"},
            {"tag":"Emby","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Emby.srs","download_detour":"direct"},
            {"tag":"Epic","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Epic.srs","download_detour":"direct"},
            {"tag":"Steam","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Steam.srs","download_detour":"direct"},
            {"tag":"Spotify","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Spotify.srs","download_detour":"direct"},
            {"tag":"Bahamut","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Bahamut.srs","download_detour":"direct"},
            {"tag":"Netflix","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Netflix.srs","download_detour":"direct"},
            {"tag":"Disney","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/Disney.srs","download_detour":"direct"},
            {"tag":"PrimeVideo","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/PrimeVideo.srs","download_detour":"direct"},
            {"tag":"HBO","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/HBO.srs","download_detour":"direct"},
            {"tag":"TikTok","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Repcz/Tool/raw/X/sing-box/Rules/TikTok.srs","download_detour":"direct"},
            {"tag":"ChinaDomain","type":"remote","format":"binary","url":"https://git.repcz.link/raw.githubusercontent.com/MetaCubeX/meta-rules-dat/sing/geo/geosite/cn.srs","download_detour":"direct"},
            {"tag":"ChinaIP","type":"remote","format":"binary","url":"https://git.repcz.link/github.com/Loyalsoldier/geoip/raw/release/srs/cn.srs","download_detour":"direct"},
            {"tag":"geolocation-!cn","type":"remote","format":"binary","url":"https://git.repcz.link/raw.githubusercontent.com/CHIZI-0618/v2ray-rules-dat/release/singbox_rule_set/geosite-geolocation-!cn.srs","download_detour":"direct"}
        ],
        "rules":[
            {"inbound":["tun-in","mixed-in"],"action":"resolve","strategy":"prefer_ipv4"},
            {"inbound":["tun-in","mixed-in"],"action":"sniff","sniffer":["http","tls","dns","quic"],"timeout":"500ms"},
            {"type":"logical","mode":"or","rules":[{"port":53},{"protocol":"dns"}],"action":"hijack-dns"},
            {"protocol":["quic"],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"and","rules":[{"port":443},{"network":"udp"}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"or","rules":[{"type":"logical","mode":"or","rules":[{"domain_keyword":"analytics"},{"domain_keyword":"doubleclick"}]},{"type":"logical","mode":"and","rules":[{"domain_keyword":"ra7"},{"domain_keyword":"xyz"}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"or","rules":[{"type":"logical","mode":"or","rules":[{"domain_keyword":"apidns"},{"domain_keyword":"httpdns"}]},{"type":"logical","mode":"and","rules":[{"domain_keyword":"dns"},{"type":"logical","mode":"or","rules":[{"domain_keyword":"jd"},{"domain_keyword":"weibo"},{"domain_keyword":"qq"}]}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"and","rules":[{"type":"logical","mode":"or","rules":[{"domain_keyword":"biliapi"},{"domain_keyword":"bilibili"},{"domain_keyword":"bilivideo"}]},{"type":"logical","mode":"or","rules":[{"domain_keyword":"-live-tracker-"},{"domain_keyword":"p2p"},{"domain_keyword":"pcdn"},{"domain_keyword":"cmask"},{"domain_keyword":"cm"},{"domain_keyword":"mcdn"}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"and","rules":[{"network":"udp"},{"type":"logical","mode":"and","rules":[{"domain_keyword":"p2p"},{"domain_keyword":"douyu"}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"and","rules":[{"type":"logical","mode":"or","rules":[{"domain_keyword":"p2p"},{"domain_keyword":"mobgslb"},{"domain_keyword":"szbdyd"}]},{"type":"logical","mode":"or","rules":[{"domain_keyword":"huya"},{"domain_keyword":"tbcache"},{"domain_keyword":"com"}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"or","rules":[{"type":"logical","mode":"and","rules":[{"domain_keyword":"live"},{"domain_keyword":"ksapisrv"}]},{"type":"logical","mode":"and","rules":[{"network":"udp"},{"port":8443}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"and","rules":[{"network":"udp"},{"type":"logical","mode":"or","rules":[{"port":6443},{"type":"logical","mode":"or","rules":[{"domain_keyword":"douyincdn"},{"domain_keyword":"ndcpp"}]}]}],"action":"reject","outbound":"reject"},
            {"type":"logical","mode":"or","rules":[{"type":"logical","mode":"and","rules":[{"network":"tcp"},{"port":[22,5228]}]},{"type":"logical","mode":"and","rules":[{"network":"udp"},{"port":123}]}],"action":"route","outbound":"direct"},
            {"process_name":["tailscaled"],"action":"route","outbound":"direct"},
            {"type":"logical","mode":"or","rules":[{"domain_keyword":"cftunnel"},{"domain_keyword":"sslip"},{"domain_keyword":"tailscale"}],"action":"route","outbound":"direct"},
            {"clash_mode":"Direct","action":"route","outbound":"direct"},
            {"clash_mode":"Proxy","action":"route","outbound":"Proxy"},
            {"rule_set":["Ads"],"action":"reject"},
            {"rule_set":["AI"],"action":"route","outbound":"AI"},
            {"rule_set":["YouTube","Google"],"action":"route","outbound":"Google"},
            {"rule_set":["Microsoft","OneDrive","Github"],"action":"route","outbound":"Microsoft"},
            {"rule_set":["Twitter"],"action":"route","outbound":"Twitter"},
            {"rule_set":["Telegram"],"action":"route","outbound":"Telegram"},
            {"rule_set":["Emby"],"action":"route","outbound":"Emby"},
            {"rule_set":["Steam","Epic"],"action":"route","outbound":"Game"},
            {"rule_set":["Bahamut","Netflix","Disney","PrimeVideo","HBO","TikTok"],"action":"route","outbound":"ProxyMedia"},
            {"rule_set":["AppleProxy"],"action":"route","outbound":"🇭🇰 HongKong"},
            {"rule_set":["geolocation-!cn"],"action":"route","outbound":"Proxy"},
            {"rule_set":["ChinaDomain","ChinaIP","Apple"],"action":"route","outbound":"direct"},
            {"ip_is_private":true,"action":"route","outbound":"direct"}
        ],
        "find_process":true,
        "auto_detect_interface":true,
        "final":"Final"
    },
    "log":{
        "disabled":false,
        "level":"info",
        "output":"sing-box.log",
        "timestamp":true
    },
    "experimental":{
        "cache_file":{
            "enabled":true,
            "store_fakeip":true
        },
        "clash_api":{
            "default_mode":"Rule",
            "external_controller":":9091",
            "external_ui":"/usr/share/sing-box/ui",
            "secret":"^_^Sin(7!a)*2|>_<|",
            "external_ui_download_url":"https://git.repcz.link/github.com/Zephyruso/zashboard/releases/latest/download/dist.zip",
            "external_ui_download_detour":"Proxy"
        }
    },
    "inbounds":[
        {
            "tag":"mixed-in",
            "type":"mixed",
            "listen":"0.0.0.0",
            "listen_port":7080,
            "set_system_proxy":false
        },
        {
            "tag":"tun-in",
            "type":"tun",
            "interface_name": "sing-box0",
            "address":[
                "172.18.0.1/30",
                "fdfe:dcba:9876::1/126"
            ],
            "platform":{
                "http_proxy":{
                    "enabled":true,
                    "server":"127.0.0.1",
                    "server_port":7080
                }
            },
            "stack":"system",
            "auto_route":true,
            "strict_route":true,
            "auto_redirect":true
        }
    ]
}
