# Service: Content Processing

The Content Processing service allows your Modifier to modify messages before it is bridged to other servers and platforms.

To enable Content Processing,&#x20;

## Functions

### `await process`

Function called by Unifier Bridge to stylize a message using the Plugin.

**Provided arguments**

* **`message`**: Message object for the content to stylize. This may be `nextcord.Message`, `revolt.Message` or `guilded.Message`.

**Expected return**

A `nextcord.Message`, `revolt.Message` or `guilded.Message` object. The object **type** must be identical to that of the provided object.

## Compatibility

Modifiers offering Content Protection service should have a minimum Unifier release requirement of **49** or above.
