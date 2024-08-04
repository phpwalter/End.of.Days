Using the above JSON data subset, I want to convert that data set into a list, by entry that has enumerated and bulleted items from each entry

- replace BOLD HTML with BOLD Markdown
- replace "\n" with " "
- if `Deck Limit` > 1 than place "false" in `Is Unique`

Use this as your map:

### JSON to Enumerated and Bulleted List Comprehensive Map

1. ### `name`
    - **Name**: `name`
        - **Traits**: `traits`
        - **Type Code**: `type_code`
        - **subtype_code**: `subname`
        - **Faction Code**: `faction_code`

    - **Card Details**:
        - **Code**: `code`
        - **Position**: `position`
        - **Quantity**: `quantity`
        - **Pack Code**: `pack_code`
        - **restrictions**: `restrictions`
        - **Deck Limit**: `deck_limit`
        - **Is Unique**: if `deck_limit` > 1 then "false" else "true"

    - **Actions**:
        - **Revelation**: Extracted from `text` (`**Revelation** ...`) if it exists, without the duplicate label
        - **Action**: Extracted from `text` (`**Action** ...` or `**Free** ...`) if it exists, without the duplicate label
        - **Reaction**: Extracted from `text` (`**Reaction** ...` or `**Free** ...`) if it exists, without the duplicate label
        - **Forced**: Extracted from `text` (`**Forced** ...`) if it exists, without the duplicate label
