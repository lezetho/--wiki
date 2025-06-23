---
description: Unifier features each supported platform has.
---

# Platform features

| Feature               | Unifier for Discord                   | Unifier for Revolt        | Unifier for Guilded                    |
| --------------------- | ------------------------------------- | ------------------------- | -------------------------------------- |
| Cross-server          | ✅                                     | ✅                         | ✅                                      |
| Cross-platform        | ✅                                     | ✅                         | ✅                                      |
| Responsiveness[^1]    | [✅ Excellent](#user-content-fn-2)[^2] | ✅ Excellent               | [✅ Excellent](#user-content-fn-3)[^3]  |
| Reply display         | ✅ Using buttons                       | ✅                         | ✅ Using added text to bridged messages |
| Posts support         | ✅                                     | ⚠️ Posting only           | ⚠️ Posting only                        |
| Global emojis support | ✅                                     | ❌                         | ❌                                      |
| Private Rooms support | ✅                                     | ✅                         | ❌ (Planned)                            |
| Custom avatar support | ✅                                     | ✅                         | ✅                                      |
| Nickname support      | ✅                                     | ✅                         | ✅                                      |
| Custom name color     | ❌ Not possible on Discord             | ✅ To-Revolt bridging only | ❌ Not possible on Guilded              |
| User/server blocking  | ✅                                     | ✅                         | ✅                                      |
| Message reporting     | ✅                                     | ❌ (Planned)               | ❌ (Planned)                            |
| Bridge medium         | Webhooks                              | Bot messages              | Webhooks                               |

[^1]: This can vary depending on multiple factors, such as but not limited to platform responsiveness and host&#x20;

    server responsiveness.

[^2]: Internal testing with Threaded Bridge v2 and Platform Multisend experiments enabled show that the time taken for Unifier Bridge v2 to bridge a message to a Discord server is between 0.08-0.10 seconds.

[^3]: As of v3, Guilded bridging performance is pretty much on par to that of Discord and Revolt. However, responsiveness can still vary. This is a Guilded thing, it's not within our control.
