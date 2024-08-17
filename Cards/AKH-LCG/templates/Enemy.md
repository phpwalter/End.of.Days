Using the above JSON data subset, I want to convert that data set into a list, by entry that has enumerated and bulleted items from each entry. Display just the first record converted. Ask if I would like to make changes or, if satisfied, create a download file containing all records.

- replace BOLD HTML with BOLD Markdown
- replace "\n" with " "

Use this as your map::

### JSON to Enumerated and Bulleted List Comprehensive Map

1. ###  `name`
   - **Name**: `name`
     - **Traits**: `traits`
     - **Type Code**: `type_code`
     - **Faction Code**: `faction_code`
     - **"text"**: `text`

   - **Skills**:
     - **Damage**: `enemy_damage`
     - **Evade**: `enemy_evade`
     - **Fight**: `enemy_fight`
     - **Horror**: `enemy_horror`

   - **Stats**:
     - **Health**: `health`

   - **Card Details**:
     - **Code**: `code`
     - **Pack Code**: `pack_code`
     - **Position**: `position`

   - **Deck Options**: `deck_options`
     - **Quantity**: `quantity`
     - **Is Unique**: if `deck_limit` > 1 then "false" else "true"
     - **Restrictions**: `restrictions` or "N/A" if `restrictions` is empty

   - **Flavor**:
     - **Text**: `flavor`
