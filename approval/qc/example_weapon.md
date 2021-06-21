# Example weapon

```js
#pragma strict_types
#include <weapon_lib.h>
inherit "obj/weapon";

void create() {
  ::create();
  if(!is_clone())
    return;

  set_name("shortsword");
  set_alias(({"light shortsword", "sword"}));
  set_short("a light shortsword");
  set_long("This shortsword has a durable wooden handle that has been "
           "expertly sanded and shaped into a comfortable grip, and then "
           "attached to a lightweight, but sharp blade.");

  set_identify("You see a blacksmith adding this sword to a pile.");
  set_smell("You smell the sword and detect the scent of polish.");
  set_taste("You taste the sword and dislike the tang of the polish.");
  set_touch("You touch the sword and admire its polished nature.");

  set_material(({"iron", "wood"}));
  set_value(481);
  set_weight(2);
  set_weapon(SHORTSWORD);
  set_difficulty(9);
  set_damage(9);
  set_parry_ac(14);
}
```
