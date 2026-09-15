# Revath's Mailbox

Revath's Mailbox replaces World of Warcraft's standard mailbox with a clean, modern interface. It combines inbox management, a spacious New Mail editor, quick bag-item attachment, and account-wide alt tracking in one window. Its searchable recipient directory can be filtered between guild members, character friends, and online Battle.net WoW characters.

## Target

- World of Warcraft Retail / Midnight 12.1 (`Interface: 120100`)
- No external libraries
- Saved data stays locally in `WTF/Account/.../SavedVariables/RevathsMailbox.lua`

## Install

1. Remove any older `AltMail`, `RevathsMail`, or `RevathsMailbox` folder from `_retail_/Interface/AddOns/`. Do not merge addon folders.
2. Copy the new `RevathsMailbox` folder into:
   `_retail_/Interface/AddOns/`
3. The final path must be:
   `_retail_/Interface/AddOns/RevathsMailbox/RevathsMailbox.toc`
4. Restart WoW or type `/reload`.
5. Make sure **Revath's Mailbox** is enabled on the character-selection AddOns screen.

## Use

- Visit any in-game mailbox. Revath's Mailbox opens instead of the standard mailbox window.
- **Inbox:** select messages, read their body, take attached items or money, return eligible mail, or delete eligible mail.
- **Open all:** collect attachments and attached money from multiple messages with one click. Mail is processed sequentially, COD messages are skipped, and the operation can be stopped at any time.
- **New Mail:** type a recipient or select one from Contacts, attach items by dragging them from bags, and optionally send money or request COD.
- **Quick Attach:** attach all available profession-material stacks, all unbound bind-on-equip items, or one localized material category such as leather, cloth, metal and stone, herbs, or enchanting supplies. At most 12 total stacks fit in one mail.
- **Contacts:** use the source menu to filter guild members, character friends, or online Battle.net WoW characters; click a row to start a message. The currently logged-in character is hidden.
- **Alts:** review every other character's last recorded money and mailbox summary; the active character is excluded.
- **Settings:** switch between two independent layouts. Modern retains the compact rectangular design; Classic expands into an old-WoW-inspired window with a raised title plaque, portrait medallion, thick rounded ornamental borders, recessed panels, beveled red controls, and parchment mail pages. The selected skin is saved account-wide.
- **Clear attachments:** remove every outgoing attachment while keeping the recipient, subject, message, and coin fields intact.
- `/revathsmailbox` or `/rmail` reopens the window while a mailbox is active.
- Click any character on the **Alts** page to address a new message to that character.

## Important game limitations

- An addon cannot query another character's mailbox remotely. Alt data is learned only when that character logs in; mailbox totals are refreshed only when that character visits a mailbox.
- Revath's Mailbox cannot send mail while no mailbox is open.
- Recipient and faction/realm restrictions are enforced by Blizzard's servers.
- Battle.net characters are available only while the friend is online in WoW on the current game project and region; Blizzard does not expose a reliable mailable character name while that friend is offline.
- Blizzard limits how quickly mailbox operations can be repeated. Open All uses Blizzard's mailbox queue state to collect messages sequentially; sending mail always requires a separate player click.
- Quick Attach considers only unlocked items in the character's equipped bags and reagent bag. It never reads bank or warband-bank contents at a mailbox, and the final Send action always requires a separate click.
- Quick Attach fills the next free outgoing-mail slots in order. Items that Blizzard marks as bound, locked, or otherwise non-mailable are skipped.
- The Battle.net Community API linked in the request is a web-service API for game/profile data. It does not expose the live in-game mailbox; Revath's Mailbox uses the in-client UI API instead.

## Troubleshooting

- If the default mailbox appears, update the `## Interface` value in `RevathsMailbox.toc` to the number shown by `/dump select(4, GetBuildInfo())`, then reload.
- If guild members are initially missing, wait a moment for the guild roster to arrive and reopen the Contacts tab.
- Enable **Display Lua Errors** in WoW's options when reporting a problem, and include the complete error text.

## Privacy

Revath's Mailbox does not use the network, Battle.net OAuth, or external services. Its SavedVariables contain character names, realm names, last-known money, and mailbox summary counts.

## Artwork

- `Media/Icon.tga` is the branded, transparent addon-list icon.
- `Media/IconSmall.tga` is the text-free transparent icon used inside the mailbox window for better readability at small sizes.
- `Media/RevathsMailbox-Logo.png` is the full-resolution transparent logo with the addon name.

## Releases

Pushing a tag such as `v1.9.1` runs the GitHub Actions release workflow. It packages the addon with `RevathsMailbox` as the ZIP's top-level folder, uploads the build as a workflow artifact, and attaches the same ZIP to a generated GitHub Release.

## Support

If you would like to support my work, you can always show a little gratitude and buy me a coffee, but remember, it is not mandatory and I do not live from donations. 
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://buymeacoffee.com/revath)
