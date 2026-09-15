# Changelog

## 1.9.1

- Hide the currently logged-in character from the Alts tab.
- Exclude the current character from Contacts even when it is discovered through guild, character-friend, or Battle.net sources.

## 1.9.0

- Add an Inbox Open all button for collecting attachments and attached money from multiple messages.
- Process messages sequentially using Retail's mailbox command state instead of issuing simultaneous loot requests.
- Skip COD mail automatically, provide progress feedback, and allow the operation to be stopped.
- Stop safely when the mailbox closes or a mail action fails.

## 1.8.0

- Automatically use the first attached item's name as the mail subject when the Subject field is empty.
- Preserve every subject entered manually and never replace non-empty text.

## 1.7.9

- Refresh the selected mail preview whenever the inbox contents change.
- Clear removed attachment textures, counts, tooltips, and click handlers from empty slots.
- Recheck the selected message shortly after manually taking an attachment.

## 1.7.8

- Show the Settings author value simply as `Revath#2331`.
- Stop the logout event from replacing a confirmed character balance with a shutdown-time zero.
- Refresh the character balance after bag data loads as an additional reliable snapshot point.

## 1.7.7

- Raise the Classic title plaque slightly so the title sits vertically centered within it.
- Draw the plaque above the mailbox window border so the window correctly recedes behind the ornament.

## 1.7.6

- Enlarge the Classic ornamental title plaque while preserving the aligned title and surrounding layout.

## 1.7.5

- Enlarge the aligned Classic title plaque slightly for a stronger frame around the title.
- Preserve a known character balance while WoW's login data is still initializing.
- Refresh character money after entering the world so real balances, including zero, are stored accurately.

## 1.7.4

- Pull the Inbox Delete button inward by tightening the action-button spacing.
- Shorten Classic Contacts and Alts rows so their right borders remain visible before the scrollbar.
- Move the Classic title and subtitle into alignment with the raised title plaque.

## 1.7.3

- Remove the misaligned minimap tracking ring from the top-left Classic branding and realign the addon icon.
- Fit all Quick Attach and Send buttons within the Classic sidebar's actual inner width.
- Resize the material-type popup to match the Classic sidebar buttons.
- Move Contacts and Alts WRITE actions inward so they clear the row edge and scrollbar.

## 1.7.2

- Crop `QuestBG` to its painted parchment region so the texture fills the complete mail surface without orange remainder blocks.
- Center the complete Classic tab strip beneath the centered title plaque.
- Resize and realign the top-left icon inside its portrait medallion.
- Preserve the existing content-panel and footer alignment grid.

## 1.7.1

- Fix the startup crash caused by passing `nil` to Retail's `Button:SetNormalTexture` method while constructing Modern buttons.
- Clear existing Classic button textures through their texture regions instead.
- Always construct the addon in the safe Modern state before applying the saved skin.
- Add protected skin application with automatic fallback to Modern when a Classic-only operation fails.

## 1.7.0

- Turn Classic into a separate presentation layer instead of a palette swap.
- Add a reshaped Classic window geometry with thicker rounded ornamental outer and panel borders while keeping it safe for the existing UI scale.
- Add a raised centered title plaque and portrait medallion treatment.
- Add wider Classic tab spacing and deeper content insets.
- Replace flat Classic controls with Blizzard's beveled panel-button textures and distinct selected states.
- Keep the Modern layout dimensions and flat control styling unchanged.

## 1.6.1

- Make every Classic frame fully opaque so the 3D world cannot bleed through the mailbox.
- Stop tiling the quest parchment texture, which caused transparent gaps and repeated parchment strips.
- Stretch a single parchment layer across each letter surface over a solid warm backing.
- Tone down the parchment brightness and retain Blizzard's ornamental dialog border.

## 1.6.0

- Rebuild the Classic skin around Blizzard's traditional dialog border, dark inset panels, red controls, gold highlights, and parchment letter texture.
- Use dark ink on parchment surfaces while retaining the existing Modern appearance.
- Add a Clear attachments button that removes all outgoing items without clearing the written mail or money fields.

## 1.5.0

- Fix Quick Attach by passing each destination attachment-slot number to the mail API.
- Verify each attachment before advancing and report items that could not be mailed.
- Add a persistent Settings tab with switchable Modern and Classic skins.
- Add author Revath, BattleTag Revath#2331, and the current addon version to Settings.

## 1.4.0

- Remove Alts from the Contacts directory and source menu; alt recipients remain on their dedicated tab.
- Add Quick Attach buttons for all profession materials and all unbound bind-on-equip items.
- Add a localized material-type menu generated from the player's bags and sorted by category.
- Attach up to the available 12 outgoing-mail slots while keeping Send as a separate player action.
- Use a fixed-height message container so the New Mail body visibly fills its intended area.

## 1.3.0

- Rename the Compose tab to New Mail.
- Add a contact-source menu for All Contacts, Guild Members, Battle.net Characters, Character Friends, and Alts.
- Add online Battle.net WoW characters from the current game project and region to the recipient directory.
- Refresh Contacts when Battle.net friend presence changes.
- Add a concise three-sentence addon description.

## 1.2.0

- Merge duplicate alt records created by differently formatted realm keys.
- Delay character database initialization until player identity is available.
- Make every character row clickable and open Compose with that character selected.
- Correct the Compose layout so Recipient, Subject, Message, and Attachments no longer overlap.
- Give the message body a full-height multiline editor.
- Add visible Gold, Silver, and Copper labels above their respective fields.
- Suppress Blizzard's mailbox before and after its delayed display event.

## 1.1.0

- Rename the addon to Revath's Mailbox.
- Add branded and compact transparent artwork.

## 1.0.0

- Initial mailbox replacement, contact directory, and account-character dashboard.
