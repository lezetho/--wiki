---
description: Comparing Unifier's speed with that of other similar bots.
---

# Benchmarks

The tool is [open-source](https://github.com/greeeen-dev/bridgemark/), so you can conduct your own testing if you're skeptical about our results (and correct us if we made a mistake somewhere) and verify that we haven't added any biases whatsoever.

## Bots we're comparing

We'll be comparing 6 bots for this comparison:

* Unifier (v3.7.1 unmodified, open source, self hosted)
* Tunnels.gg (unmodified, closed source, public instance)
* Connections Bot/ComBot (unmodified, closed source, public instance)
* Bolt (v0.7.4 patched, open source, self hosted)
* Silly Chat (v2.2.6 patched, open source, self hosted)
* InterChat (v4.1.0 unmodified, open source, public instance)

If a bot was patched by us, we've described our changes in [Things to note](benchmarks.md#things-to-note).

## Benchmarks

For this experiment, we sent a single dot (".") in connected channels to see how long it would take each bot to bridge it.

### Results table

The data below is the average time taken to bridge a message to one server (Single) and three servers (Multi) over three trials, measured in milliseconds (0.001 seconds). **Lower is better.**

<table data-full-width="false"><thead><tr><th>Category</th><th>Unifier</th><th width="127">Tunnels.gg</th><th>ComBot</th><th>Silly Chat</th><th>Bolt</th><th>InterChat</th></tr></thead><tbody><tr><td>Single</td><td><p><a data-footnote-ref href="#user-content-fn-1"><strong>1</strong></a><a data-footnote-ref href="#user-content-fn-2"><strong>73.67</strong></a> </p><p><a data-footnote-ref href="#user-content-fn-3">±21</a></p><p></p><p>B: <a data-footnote-ref href="#user-content-fn-4"><strong>157</strong></a><br>W: <a data-footnote-ref href="#user-content-fn-5"><strong>199</strong></a></p></td><td><strong>310.67</strong><br>±11<br><br>B: <strong>302</strong><br>W: <strong>324</strong></td><td><strong>158.33</strong> 👑<br>±10<br><br>B: <strong>149</strong><br>W: <strong>169</strong></td><td><strong>369.00</strong><br>±10.5<br><br>B: <strong>356</strong><br>W: <strong>377</strong></td><td><strong>339.00</strong><br>±23.5<br><br>B: <strong>322</strong><br>W: <strong>369</strong></td><td><strong>565.33</strong><br>±26<br><br>B: <strong>537</strong><br>W: <strong>589</strong></td></tr><tr><td>Multi (3 servers)</td><td><p><strong>212.00</strong> 👑</p><p>±75<br><br>B: <strong>140</strong><br>W: <a data-footnote-ref href="#user-content-fn-6"><strong>290</strong></a></p></td><td><strong>462.67</strong><br>±180<br><br>B: <strong>312</strong><br>W: <strong>672</strong></td><td><p><strong>235.22</strong></p><p>±131.5<br><br>B: <strong>141</strong><br>W: <strong>404</strong></p></td><td><strong>653.67</strong><br>±266<br><br>B: <strong>396</strong><br>W: <strong>928</strong></td><td><strong>530.22</strong><br>±230.5<br><br>B: <strong>320</strong><br>W: <strong>781</strong></td><td><strong>570.78</strong><br>±75.5<br><br>B: <strong>486</strong><br>W: <strong>637</strong></td></tr></tbody></table>

(Note: you may need to scroll to see all entries.)

### Graphs

<div data-full-width="true"><figure><img src="../.gitbook/assets/Screenshot 2024-11-27 at 13.28.10.png" alt=""><figcaption><p>A column graph showing the performance of the 6 bots compared. Lower is better.</p></figcaption></figure></div>

<figure><img src="../.gitbook/assets/Screenshot 2024-11-27 at 13.28.18.png" alt=""><figcaption><p>A column graph showing the performance of the top 2 bots. Lower is better.</p></figcaption></figure>

## Calculations

The averages were derived from the mean average of the three trials for each category for each bot.

## Things to note

We try to keep our data as consistent, accurate, and bias-free as possible, but there's still some things you probably want to know about this experiment.

* Unifier instance used for testing was hosted in **Canada**, while Bolt and Silly Chat instances used for testing were hosted in **Germany** due to compatibility issues with the former host. We do not know where the Tunnels.gg and Connections Bot instances were hosted in.
* As Tunnels.gg and Connections Bot are closed source, **we could not get access to private instances for testing**, so we had to use public instances.
  * This means that our private instances were connected to much less servers than Tunnels.gg's and Connections Bot's public instances, which were each connected to thousands. However, both Tunnels.gg and Connections Bot were most likely running on hosts with much more resources than the host we used, since more resources would be required to keep up with a larger server count than just a [dual-core 4GB RAM host](#user-content-fn-7)[^7]. Therefore, we decided to not take the server count difference into account, as the resources difference would balance it out.
* Although InterChat is open source, we could not self-host it due to lack of proper documentation for self hosting. Therefore, we decided to use the public instance instead.
* For some bots, we actually did more than three trials until we could get three trials that gave consistent data. This so we can measure what the bots are able to achieve on a consistent basis without giving any of them unfair bonuses or penalties for inconsistent performance.
* We wanted to test the bridging performance of files, but we decided to not do this as a fair testing environment was impossible. While Unifier relays replicas of files to servers, other bots we compared sent the attachment link instead. Testing the file bridging speed for bots that send attachment links would be the same as testing the text bridging performance again.
* Our version of Bolt was modified, as the original version would not run on our system. We added very minor changes, though, as we only had to add the `jbr:` prefix at the front of many import statements to get the bot to load the necessary libraries.
* Our version of Silly Chat was modified, as the original version would refuse to run on our system. For example, we've changed the Discord wrapper from discord.py to Nextcord due to the bot hanging on boot and removed AI commands so we don't have to configure AI API endpoints and keys.

## So...what's the conclusion?

Both Unifier and Connections Bot showed very similar performance, and **they both take 1st place on our benchmarks**. While Connections Bot beat Unifier in single bridge by about 20 milliseconds, Unifier beat Connections Bot in multi bridge also by about 20 milliseconds. This shows that we (UnifierHQ and Soup Creations) optimized our respective bots (Unifier and Connections Bot) insanely well that we deserve to share the title of the fastest bridge bots on Discord, which is honestly amazing.

Tunnels.gg is also plenty fast, taking only 310.67 milliseconds for the single bridge test and 462.67 milliseconds for the multi bridge test. All of the top three bots' performance are well within what we would consider acceptable for most use cases.

Bolt was somewhat similar to Tunnels.gg on the single bridge test, but it seems to have struggled on the multi bridge test. Although this is acceptable for smaller rooms/connections where only a few servers are connected at a time, it may be a bottleneck for larger rooms/connections.

InterChat and Silly Chat, on the other hand, are very behind the competition. The time taken to bridge a message to a server is long enough to cause noticeable issues during use, and it should be avoided if possible. For InterChat, this seems to be due to the bot taking too long to start bridging the message and not lack of concurrency as both single and multi bridge times were quite similar, while for Silly Chat, it's a mix of both as the multi bridge time was much higher than the single bridge time.

What is even more concerning for Silly Chat is that the test was conducted in a **better-case environment than the developer's own instance**, and in the latter we witnessed the bot taking **seconds or minutes until the message started bridging**. We're not sure if this is because he was running the unmodified version, or if he had a significantly worse setup, but this is still very far from acceptable, even for smaller use cases.

If you're looking for a bridge bot for your community, we'd (obviously) recommend **Unifier** for its record-holding bridging speeds and excellent versatility. However, we would also certainly recommend **Connections Bot (ComBot)** and **Tunnels.gg** as **very solid alternatives**, as they're also plenty fast and feature-packed (although they lack cross platform bridging) that they also fit well for communities of any size.

Whichever bot you may end up using, we hope you enjoy your cross-server or cross-platform chatting experience!

## Acknowledgements

Thank you to MrTomato (developer of Connections Bot) for giving us feedback on BridgeMark to help make our benchmarks more accurate!

[^1]: Average time taken to bridge messages.

[^2]: Average time taken to bridge messages.

[^3]: Uncertainty (calculated using (max-min)/2). Lower uncertainties suggest better consistency across servers.

[^4]: Shortest time taken to bridge one message to a connected channel, **not** shortest average time taken for each trial.

[^5]: Longest time taken to bridge one message to a connected channel, **not** longest average time taken for each trial.

[^6]: For some bots, the worst multi-bridge performance may be significantly higher than the best performance and average performance, as they bridge to servers sequentially rather than concurrently.

[^7]: These are the specifications of the host we used to run our private instances.
