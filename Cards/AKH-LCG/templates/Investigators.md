
### JSON to Enumerated and Bulleted List Comprehensive Map

1. ###  `name`: `subname`
  - **Name**: `name`
    - **Subname**: `subname`
    - **Traits**: `traits`
    - **Type Code**: `type_code`
    - **Faction Code**: `faction_code`

  - **Skills**:
    - **Agility**: `skill_agility`
    - **Combat**: `skill_combat`
    - **Intellect**: `skill_intellect`
    - **Willpower**: `skill_willpower`

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
