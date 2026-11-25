# Shotcut Motion Graphics

Create editable motion graphics from a conversation with Claude. Start with a product intro, quote card, or animated statistic, preview it, revise the text and timing, inspect individual frames, and export an MP4.

Operated by Pro Stack Labs at [shotcut.ai](https://shotcut.ai). It is separate from the open-source Shotcut desktop video editor.

## Use it

Add the plugin, then connect Shotcut and sign in when Claude asks. Guides and templates work without an account; creating and opening projects needs one. Try:

- Create a product-intro template project and show its preview.
- Change the headline to "Launch day" and make it two seconds longer.
- Validate this project, show the frame at 3 seconds, and render an MP4.

Renders are limited to 180 seconds, 1080p and 30 fps. Each project keeps its three newest renders, so download the ones you need. Current limits are on the [support page](https://shotcut.ai/support).

## What it contains

- One skill, `shotcut-motion`, with the steps for creating, checking and exporting a project.
- One remote MCP server, `https://shotcut.ai/mcp`.

The plugin runs no code on your computer. It has no hooks, scripts, or package installs.

## Data

Claude sends the tool inputs you approve to your Shotcut account at shotcut.ai: project titles, composition source, edit summaries, and any public media URL you ask to import, which Shotcut's server then downloads. Sign-in uses OAuth through Clerk. Shotcut does not receive your conversation history and does not train AI models on your content. It renders HTML and CSS compositions and does not call a generative image, video, or audio model.

Projects are private by default, and a project link alone gives no access. Projects stay until you delete them, with older versions, frames, and renders pruned as described on the support page. Delete your account data at [shotcut.ai/account](https://shotcut.ai/account). See the [privacy policy](https://shotcut.ai/privacy), [terms](https://shotcut.ai/terms), and [service providers](https://shotcut.ai/subprocessors).

## Support

support.shotcut@prostacklabs.com
