Using the above JSON data subset, I want to convert that data set into a list, by entry that has enumerated and bulleted items from each entry. Display just the first record converted. Ask if I would like to make changes or, if satisfied, create a download file containing all records.

- replace BOLD HTML with BOLD Markdown
- replace "\n" with " "

Use this as your map:

### JSON to Enumerated and Bulleted List Comprehensive Map

1. ###  `name`: `subname`
  - **Name**: `name`
    - **Subname**: `subname`
    - **Traits**: `traits`
    - **Type Code**: `type_code`
    - **Faction Code**: `faction_code`

  - **Skills**:
    - **Agility**: `skill_agility` or "N/A" if `skill_agility` is empty
    - **Combat**: `skill_combat` or "N/A" if `skill_combat` is empty
    - **Intellect**: `skill_intellect` or "N/A" if `skill_intellect` is empty
    - **Willpower**: `skill_willpower` or "N/A" if `skill_willpower` is empty
    - **Wild**: `skill_wild` or "N/A" if `skill_wild` is empty

  - **Stats**:
    - **Health**: `health`
    - **Sanity**: `sanity`

  - **Flavor**:
    - **Front Text**: `flavor`
    - **Back Flavor**: `back_flavor`

  - **Card Details**:
    - **Code**: `code`
    - **Position**: `position`
    - **Quantity**: `quantity`
    - **Pack Code**: `pack_code`

  - **Deck Options**: `deck_options`
    - **Deck Size**: Extracted from `back_text` (`<b>Deck Size</b>: 30.`)
    - **Deck Requirements**: `deck_requirements`
    - **Deck Limit**: `deck_limit`
    - **Option 1**:
        - **Faction**: `deck_options[0].faction`
        - **Level**: `deck_options[0].level`
    - **Option 2**:
        - **Faction**: `deck_options[1].faction`
        - **Level**: `deck_options[1].level`
    - **Is Unique**: if `deck_limit` > 1 then "false" else "true"
    - **Double Sided**: `double_sided`
    - **Deckbuilding Options**: Extracted from `back_text` (`<b>Deckbuilding Options</b>: ...`)
    - **Deckbuilding Requirements**: Extracted from `back_text` (`<b>Deckbuilding Requirements</b> ...`)

  - **Text**: `text`
    - **Reaction**: Extracted from `text` (`[reaction] ...`)
    - **Elder Sign Effect**: Extracted from `text` (`[elder_sign] effect: ...`)
