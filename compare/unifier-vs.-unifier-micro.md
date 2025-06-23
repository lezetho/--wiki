# Unifier vs. Unifier Micro

Recently (as of first writing this page), we created Unifier Micro, a lightweight version of Unifier with only the core features. It is designed for smaller communities who have very limited resources, so they can still bring their communities together without needing too much resources.

As Unifier Micro heavily cuts down on caching, it will use the CPU and network more often compared to Unifier.

| Feature                                          | Unifier                               | Unifier Micro                                                |
| ------------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ |
| Cross-server[^1]                                 | ✅                                     | ✅                                                            |
| Cross-platform[^2]                               | ✅                                     | ❌                                                            |
| Speed[^3]                                        | [✅ Excellent](#user-content-fn-4)[^4] | Decent                                                       |
| [Message replying](#user-content-fn-5)[^5]       | ✅                                     | ✅                                                            |
| [Posts support](#user-content-fn-6)[^6]          | ✅                                     | ❌                                                            |
| [Global emojis support](#user-content-fn-7)[^7]  | ✅                                     | ❌                                                            |
| [Custom avatar support](#user-content-fn-8)[^8]  | ✅                                     | ❌                                                            |
| [Nickname support](#user-content-fn-9)[^9]       | ✅                                     | ❌                                                            |
| [User/server blocking](#user-content-fn-10)[^10] | ✅                                     | ✅                                                            |
| [Message reporting](#user-content-fn-11)[^11]    | ✅                                     | ❌                                                            |
| Setup[^12]                                       | ✅ Easy                                | [✅ Eas**ier**](#user-content-fn-13)[^13]                     |
| [Memory usage](#user-content-fn-14)[^14]         | Varies                                | [✅ Varies, but lower than Unifier](#user-content-fn-15)[^15] |
| [Target users](#user-content-fn-16)[^16]         | Communities of any size               | Small communities                                            |
| [Bridge medium](#user-content-fn-17)[^17]        | Hybrid[^18]                           | Webhooks                                                     |

[^1]: Ability to bridge from a server to a different server on the same platform.

[^2]: Ability to bridge from a server to a different server on a completely different platform (e.g. Discord to Revolt).

[^3]: Bridging speed, does not take general bot responsiveness into account unless it affects bridging speeds.

[^4]: Thanks to concurrent processing and performance optimization libraries and techniques, Unifier can bridge messages at extremely fast speeds.

[^5]: Ability to show message replies.

[^6]: Support for Posts.

[^7]: Ability to allow users to use emojis from opted-in servers from any connected server.

[^8]: Ability to set a custom profile picture for Unifier without changing your actual profile picture.

[^9]: Ability to set a custom display name for Unifier without changing your actual display name or server nickname.

[^10]: Ability to let server moderators block users or servers from bridging messages to their server.

[^11]: Ability to easily and anonymously report abusive messages to instance moderators.

[^12]: Difficulty of installation and setup process.

[^13]: Unifier Micro has the upper edge thanks to having less things to set up and maintain.

[^14]: Overall memory usage, lower is better.

[^15]: Unifier Micro does not have support for cogs and Plugins whatsoever, which helps reduce overall memory usage.

[^16]: Target audience for the products.

[^17]: Medium used to bridge messages to a platform.

[^18]: Unifier uses webhooks on platforms like Discord and Guilded to bridge messages, while it uses regular bot messages on platforms like Revolt.
