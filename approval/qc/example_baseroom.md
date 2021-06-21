# Example baseroom

```C
#pragma strict_types
inherit "room/room";

void create() {
  ::create();

  set_light(1);
  set_search("You search around, but discover no secrets.");
  set_smell("You smell around and detect a woody scent.");
  set_sound("You listen intently and hear conversation nearby.");

  add_senses(({"floor", "walls", "wall", "ceiling"}), ([
    "item": "You examine the barracks and admire the quality construction.",
    "noget": "You try to take the barracks, but it is not possible.",
    "search": "You search the barracks, but discover no secrets.",
    "smell": "You smell the barracks and the scent of wood overwhelms you.",
    "sound": "You listen to the barracks and hear conversations nearby.",
    "taste": "You taste the barracks and dislike the woody tang.",
    "touch": "You touch the barracks and admire the quality construction."
  ]));

  add_sound(({"conversations", "conversation",}),
    "You listen to the conversation, but cannot hear what is being said.");
}

int query_x_coord() { return 0; }
int query_y_coord() { return 0; }
```
