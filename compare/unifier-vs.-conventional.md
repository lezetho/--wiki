# Unifier vs. Conventional

Something I asked myself when making Unifier was, "why do I need to make a whole new bot when I can just get something off the shelf to do it?"

And the answer was simple. Our goal was to unite many communities, not just few. And with conventional bots, we could not do that. So like how I did with Nevira and how [Ente did with Ente Photos (not sponsored)](https://ente.io/about), I thought I'd just build my own bot that ticks the boxes I needed.

**This comparison is not meant to criticize conventional bridge bots in any way**, I only made this to show why I made Unifier instead of using an existing bot.

| Feature                                          | Unifier                               | Conventional                                           |
| ------------------------------------------------ | ------------------------------------- | ------------------------------------------------------ |
| Cross-server[^1]                                 | ✅                                     | ⚠️ Some only support bridging between two servers only |
| Cross-platform[^2]                               | ✅                                     | ❌                                                      |
| Speed[^3]                                        | [✅ Excellent](#user-content-fn-4)[^4] | [✅ Good](#user-content-fn-5)[^5]                       |
| [Message replying](#user-content-fn-6)[^6]       | ✅                                     | ✅                                                      |
| [Global emojis support](#user-content-fn-7)[^7]  | ✅                                     | [⚠️ Varies](#user-content-fn-8)[^8]                    |
| [Custom avatar support](#user-content-fn-9)[^9]  | ✅                                     | ❌                                                      |
| [Nickname support](#user-content-fn-10)[^10]     | ✅                                     | ❌                                                      |
| [User/server blocking](#user-content-fn-11)[^11] | ✅                                     | ✅                                                      |
| [Message reporting](#user-content-fn-12)[^12]    | ✅                                     | [⚠️ Varies](#user-content-fn-13)[^13]                  |
| [Bridge medium](#user-content-fn-14)[^14]        | Hybrid[^15]                           | Webhooks/Hybrid[^16]                                   |

Although conventional bridge bots are simple, out-of-the-box solutions to bridge Discord servers or even other platforms, it wasn't what we really wanted. We wanted to build a community by uniting smaller communities that had similar interests as us, which wasn't something those bots could really do.

Additionally, we wanted servers to have more control over what makes it into their servers via Unifier, but this wasn't really that good in conventional bots. You could ask the server moderators from the other side of the bridge to mute a troublemaker, but if they aren't cooperative then you would only have the choice to unlink the server or let it slide. We didn't want just these as moderation, so we added server-side blocking to Unifier so recipients are the ones deciding what makes the final cut, not the sender.

We also added some goodies such as cross-server emojis and custom avatars, so you can use paywalled features you couldn't use before without paying. For example, if you're in server A but not in server B where all the juicy emojis belong, you can't use the emojis you wanted. And even if you had access to server B, you couldn't use them in server A without paying. So instead, we added global emojis so you can just use them in whatever server you fancy.

And with these features, I think we've ticked almost all of the boxes we wanted to tick. There's definitely more boxes we want to tick, but the best thing is we, as the developers, have control over what we do indeed tick. So expect more from Unifier in the near future!

[^1]: Ability to bridge from a server to a different server on the same platform.

[^2]: Ability to bridge from a server to a different server on a completely different platform (e.g. Discord to Revolt).

[^3]: Bridging speed, does not take general bot responsiveness into account unless it affects bridging speeds.

[^4]: Thanks to concurrent processing and performance optimization libraries and techniques, Unifier can bridge messages at extremely fast speeds.

[^5]: This can vary depending on the bridge bot you use. But from our research, many of the most popular bridge bots for Discord are still quite fast (not as fast as Unifier, though), so chances are it'll likely be fast enough for regular use.

[^6]: Ability to show message replies.

[^7]: Ability to allow users to use emojis from opted-in servers from any connected server.

[^8]: Some bots do this, but some of them may require you to pay before you can use this feature. Unifier has this feature for free.

[^9]: Ability to set a custom profile picture for the bridge without changing your actual profile picture.

[^10]: Ability to set a custom display name for the bridge without changing your actual display name or server nickname.

[^11]: Ability to let server moderators block users or servers from bridging messages to their server.

[^12]: Ability to easily and anonymously report abusive messages to instance moderators.

[^13]: Only some bots have this feature. We believe that all bots should have an integrated message reporting interface, so it's easier for users to report harmful content to moderators.

[^14]: Medium used to bridge messages to a platform.

[^15]: Unifier uses webhooks on platforms like Discord and Guilded to bridge messages, while it uses regular bot messages on platforms like Revolt.

[^16]: This will depend on the cross-platform capabilities of the bridge bot. For example, if it doesn't bridge to Revolt, it will only need to use Webhooks. But if it needs to bridge to Revolt, it will use Webhooks for Discord and bot messages with Masquerade for Revolt.
