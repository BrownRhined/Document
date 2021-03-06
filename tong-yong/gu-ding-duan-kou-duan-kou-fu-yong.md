# 公共端口

### 概述 {#概述}

公共端口是 SSR 协议中的特性，与一般模式不同之处是允许多个用户使用同一个端口，而不是使用为每个用户单独分配的端口。

### 使用场景 {#使用方法}

1. 通常建议所有人都使用个人端口。
2. Surge 用户：由于 Surge 只有 iOS / macOS 版，其他平台对 ShadwsocksR 支持度更好，所以需要使用公共端口。

### 优势 {#优势}

1. 某些组织或企业的内部网络可能有行为管理，并配置了端口限制，如只允许访问 HTTP（80 端口）和 HTTPS（443 端口）。这时使用一般的配置就无法连接，使用公共端口则可以正常连接。
2. 某些运营商可能对非常用端口，特别是高位端口进行限速（因为高位端口多数被用于 BitTorrent）。使用常见端口可能对某些 ISP 的 QoS 有正面效果。

### 劣势 {#劣势}

1. SSR 的公共端口实现存在性能问题，使用此模式可能无法获得最佳性能。
2. 公共端口不允许自定义协议。此外，出于安全考虑，我们的公共端口使用了较为复杂的协议插件，这可能导致低性能平台（如一般路由器）出现性能问题。
3. 此模式可能容易出现 TCP 连接异常中断问题。
4. 此模式存在 UDP 性能问题。

