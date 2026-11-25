---
name: shotcut-motion
description: Create, revise, preview, and export editable motion graphics with Shotcut. Use when the user asks for a motion video, product intro, quote card, or animated statistic in Shotcut, or shares a Shotcut project link.
---

Use the Shotcut connector's tools. Keep to the design and scope the user asked for.

## Start a project

1. Call `list_templates` when a starter could fit, then `create_project` with its `templateId`. Otherwise call `create_project` without one.
2. For custom source, look up the composition format in the reference documentation from `get_guide` (topics `workflow` and `contract`), then call `write_files`.
3. Import media the user supplies with `add_media`, and use the relative asset path it returns.

## Revise a project

1. Call `read_project` with the project ID or Shotcut URL. Keep any pending human edits it reports.
2. Apply the changes with `write_files` and a short summary. For a title change alone, use `update_project`.

## Check and preview

1. After source changes, call `validate` and fix its errors.
2. Call `snapshot_frame` at two to four key moments within the duration, look at the images, and fix visible defects.
3. Call `open_editor` when the user wants the playable preview.

## Export

Call `render` when the user asks for an MP4, then `get_render` to report its real status and website link. Report a failed render before retrying it. A project keeps its three newest renders, so a new render can delete an older one. Downloading needs sign-in on the website as the project owner.

## Accounts and access

- Guides and templates are public. Everything else needs a linked Shotcut account; when a tool asks for sign-in, let the user connect.
- Use `list_projects` for the user's own saved projects.
- Links and IDs grant no access by themselves. If a project is not found, say so.
- Never ask for passwords or tokens in chat.
- There is no deletion tool. Send the user to https://shotcut.ai/account to delete their data.
