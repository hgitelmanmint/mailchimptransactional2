# Mailchimp Transactional — Demo Docs Site

A fully built-out Mintlify docs site themed as Mailchimp Transactional, built for the Mintlify onsite demo. Three tabs (Documentation, API Reference, Changelog), a working API playground driven by a real OpenAPI spec, version switcher (1.0 / 1.1 / 1.3), and MailChimp yellow theming.

## What's in here

```
docs.json                      Site config: theme, navigation, versions
index.mdx                      Landing page (the first screen they see)
quickstart.mdx                 Send your first message in 5 minutes
authentication.mdx             API key auth
guides/
  sending-email.mdx            The message object in depth
  templates.mdx                Reusable templates + merge vars
  webhooks.mdx                 Event streaming
  migrating-from-1-0.mdx       Version migration (answers the versioning pain)
api-reference/
  openapi.json                 The spec that powers the playground
  messages/send.mdx            POST /messages/send  <- demo centerpiece
  messages/send-template.mdx
  messages/info.mdx
  webhooks/list.mdx
  webhooks/add.mdx
changelog.mdx                  Version history
logo/                          Light + dark logos
favicon.svg
```

## The four demo screens

1. **Landing page** — themed, on-brand. "This is what yours could look like."
2. **API Reference > Send a message** — the live playground. Answers Patrick's manual-OpenAPI pain.
3. **Version switcher** (top of nav) — answers Andre's 3-4-versions-this-year pain.
4. **Changelog** — answers "we don't even have an updated changelog."

---

## Deploy — fastest path (no local setup)

1. Create a new throwaway GitHub account (or use one you have).
2. Go to https://github.com/mintlify/starter and click **Use this template** to make a repo.
3. Replace the starter's contents with these files (drag-and-drop upload works in the GitHub web UI).
4. Go to https://mintlify.com/start, sign in with that GitHub account, and connect the repo.
5. Your site deploys to `https://<name>.mintlify.app`. That's your demo URL.

## Deploy — local preview (if you want to iterate)

```bash
npm i -g mint
cd mailchimp-transactional-docs
mint dev
```

Open http://localhost:3000. The preview hot-reloads as you edit.

## No-repo path

If you skip Git at onboarding, Mintlify creates a hosted repo for you and you edit in the web editor. You'd recreate these pages in the visual editor — slower, but no GitHub account needed.

---

## Before the demo — checklist

- [ ] Site is live and loads at the .mintlify.app URL
- [ ] The Send a message playground renders the request form
- [ ] Version switcher shows 1.0 / 1.1 / 1.3
- [ ] Ask your Mintlify contact to flip on **enterprise features** (assistant, llms.txt, MCP, analytics) for your account so the AI layer is visible
- [ ] Confirm `/llms.txt` resolves at your site root
- [ ] Know where the analytics view lives in the dashboard (don't demo live numbers — just navigate to it)

## Notes

- The logos are simple SVG placeholders. Swap in real MailChimp brand assets if you have them.
- The OpenAPI spec uses realistic Mailchimp Transactional endpoints and example values. The playground will format requests correctly, though live "send" calls require a real API key.
- Theme color is MailChimp yellow (#FFE01B) on near-black (#241C15).
