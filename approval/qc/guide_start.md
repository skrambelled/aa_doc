# SYNOPSIS

The following guide explains how to get started building an area in a way
that will get through Quality Control much faster and easier.

Planning is the most important step, the worst thing you can do is just build
stuff and try to connect it all later. The main reason this is a problem is
because you need to build around your base files, not the other way around.
Too many coders are inefficiently coding entire areas and then realizing
later they have no base files, and fixing then is a lot more work.

---

## DESCRIPTION

A base file room is a room that contains all of the shared features of a
certain landscape. For example, if you are creating an area like Harkke
Forest where there is outdoor ground, dirt, grass, trees, and other forest
features then all of those add_senses can all be contained in a base file
room. This way you do not have to re-write every sense in every room. This
also means we are not copy and pasting blocks of code into rooms. Build your
area around base files and you will save yourself and reviewers tons of work.

To expand on base files more, you can also create multiple base files. If you
have several forest rooms, use a forest base file. If you can leave the
forest and enter a tent then you need a tent base file that has nouns like
floor, walls, wall, ceiling, etcetera, all established so that you do not
need to repeat those in every room. Below is a visual explanation of how base
files work, and how they can even inherit each other.

```
                           BASE_room
                               |
              ---------------------------------
              |                               |
         BASE_forest                      BASE_tent
              |                               |
      -----------------                ---------------
      |               |                |             |
forests_north   forests_south     tents_large   tents_small
```

Once you have planned out all of your rooms in advance and created base
files, then you can start working on the rooms themselves which will not need
as much work because they already inherit so many add_senses.

At this point the main rooms may barely have any coding in them and might
only contain a set_short, set_long, and whatever add_senses are necessary for
the additional features that room has which the inherited base files do not.
Before you dive too deeply into working on rooms it would be a good idea to
just put together the rooms in a skeletal fashion and make sure they all load
properly first.

After the rooms are complete you move onto populating them with monsters. If
you use generic monsters, such as "a big orc" then those are the kinds of
monsters that could also use a base file if you plan on having multiples.
Again, group these up by their type, just like you did for base rooms.

When the monsters are complete you equip them by creating weapons, armours,
and treasure objects and cloning these objects to them, and then commanding
them to wield and wear the equipment.

Go into your area often and playtest the things you are creating. Spend time
exploring the area as if you were a mortal and try to Quality Control your
own project. Be sure that it all works properly and it is highly polished
before submitting it to the queue--unfinished projects will be rejected.

## EXAMPLE

- Create /w/wizardname/areaname/ as your project folder.
- Create a header file (areaname_defs.h) in your project folder.
- Create /w/wizardname/areaname/approval/ to keep documents in.
- Create a world info file in your approval directory.
- Create /w/wizardname/areaname/room/ to put base rooms and main rooms in.
- Create /w/wizardname/areaname/monster/ to put monsters in.
- Create /w/wizardname/areaname/weapon/ to put weapons in (if relevant).
- Create /w/wizardname/areaname/armour/ to put armours in (if relevant).
- Create /w/wizardname/areaname/object/ to put objects in (if relevant).
- Create a method for entering the area, such as a workroom exit.
- Read the other Quality Control guides and examples for more information.

## SEE ALSO

- [qc](./README.md)
