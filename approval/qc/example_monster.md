# Example monster

```C
#pragma strict_types
#include "../example_header.h"
#include <living.h>
inherit "obj/monster";

void create() {
  ::create();
  if(!is_clone())
    return;

  set_name("guard");
  set_alias("young guard");
  set_short("a young guard");
  set_long("This guard has been hired to help protect the mining operation "
           "from the nearby threats in the area. Although the guard is "
           "rather young, he looks determined and quite fit.");

  set_gender(MALE);
  set_race("human");
  set_level(16);
  set_al(200);
  add_money(189);

  add_spell(({"physical", 10, 15,
              "The guard lunges at you and lands a powerful hit!",
              "The guard lunges at # and lands a powerful hit!"}));

  load_chat(8, ({"The guard perks up, as if detecting something.",
                 "@common language@Those orcs don't scare me.",
                 "The guard prepares himself to go on duty."}));

  load_a_chat(8, ({"The guard lets out a grunt as he attacks.",
                   "The guard fights with determination.",
                   "The guard moves around with ease."}));

  clone_object(ARMOUR"example_armour")->move(this_object());
  command("wear breastplate");

  clone_object(WEAPON"example_weapon")->move(this_object());
  command("wield shortsword");
}
```
