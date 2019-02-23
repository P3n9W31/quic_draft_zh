
介绍
==============

QUIC (Quick UDP Internet Connection，快速UDP互联网连接) 是一个新的基于UDP的多路复用且安全的传输协议，
它从头开始设计，且为 HTTP/2 语义做了优化。尽管以 HTTP/2 作为主要的应用协议而构建，
然而 QUIC 的构建是基于传输和安全领域数十年的经验的，且实现了使它成为有吸引力的现代通用传输协议的机制。
QUIC提供了等价于HTTP/2 的多路复用和流控，等价于 TLS 的安全机制，及等价于 TCP 的连接语义、可靠性和拥塞控制。

QUIC完全运行于用户空间，它当前作为 Chromium 浏览器的一部分发布给用户，以便于快速的部署和实验。
作为基于 UDP 的用户空间传输协议，QUIC 可以做一些由于遗留的客户端和中间设备，
或旷日持久的操作系统开发和部署周期的阻碍，而被证明很难在现有的协议中部署的创新。

QUIC 的一个重要目标是通过快速的实验获得更好的传输设计相关的知识。作为结果，我们希望将其中的一些精华的改动迁移进 TCP 和 TLS，
后者通常有着长得多的迭代周期。

这份文档描述标准化前 QUIC 协议的概念设计和协议规范。补充资料描述了加密和传输握手 [QUIC-CRYPTO]，
及丢失恢复和拥塞控制 [draft-iyengar-quic-loss-recovery]。
其它资源，包括一份更详细的相关文档，可以在 Chromium 的 QUIC 主页 找到。

基于早期的部署的 QUIC 标准化建议为 [draft-hamilton-quic-transport-protocol]，
[draft-shade-quic-http2-mapping]，[draft-iyengar-quic-loss-recovery]，
和 [draft-thomson-quic-tls]。