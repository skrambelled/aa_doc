# SYNOPSIS

The following is a checklist of everything you must playtest in your area
before submitting it to the queue. It takes dozens of hours for a Quality
Control member to do a full review on a creator-sized project, and it is not
their responsibility to take your project as a rough draft and turn it into a
finished product--that is your job.

---

## DESCRIPTION

Quality Control is there check that things are standardized, logical, that
the code is sound, and a mortal will find the area to behave in expected
ways. It cannot be stressed enough that you as a coder need to thoroughly
playtest your own projects from top to bottom, or find someone that will
volunteer to do it for you, but that someone is not the Quality Control team.

Projects must be finished, and polished when they are submitted to the queue.
Any project that is in poor shape will be sent back to the author, and low
quality projects will be processed after higher quality projects, regardless
of the submission date. Follow the checklist below to ensure a quick install.

---

## EXAMPLE

### File Checklist

- All files (even plain text) must have a blank line at the end of file.
- All hidden tabs and trailing whitespace must be cleaned from every file.
- Do not use more than 1 consecutive blank line to separate code.
- Folder/File names must use snake casing (south_garden.c) over alternatives.
- Format code using the standards shown in the QC guides and examples.
- Organize the project directory, and clear out unneeded or backup files.
- Remove .c from file paths in the code, such as inside clone_object.
- Remove all unused includes and inherits from every file.
- Remove unnecessary prototypes (redirects, keywords, drama, etcetera).
- Use logical folder names, such as room, monster, object, armour, etcetera.

### General Checklist

- All communication to a player should be consistent in the wording.
- All descriptions must be written out as complete sentences.
- All rooms, monsters, objects, and daemons must use #pragma strict_types.
- All monsters and objects must use is_clone underneath ::create().
- Areas should include a Gaius exploration point.
- Asciiart should use both query_asciiart and preformat for compatibility.
- Avoid emotional explanation, such as "You do not feel like taking the box."
- Base files should be used to effectively remove duplication when relevant.
- Do not use articles (a/an/the) in the set_name or set_alias.
- Do not use contractions, unless it is in monster speech.
- Do not use formatting functions unless necessary, such as writef and sayf.
- If relevant make use of player class/race features, such as languages.
- Make intuitive clues available for mortals to solve quests/mini-quests.
- Remove functions that set the same data as the Mudlib default values.
- Run a spell check and grammar check on all files.
- Syntax for actions must use all practical options (push, press, etcetera).
- The project must use AA measurements or no measurements at all.
- The set_alias must be lowercase, and should not use commas.
- The set_name should not need to be in the set_alias too.
- The set_short must be lowercase, except for proper names.
- The set_short has a maximum length of 50 characters, no exceptions.
- UK spellings (colour, centre, etcetera) take precedence over US spellings.
- Use only a single whitespace after punctuation in a sentence.
- Use the QC hat tool to 'hatcheck' your project, and fix all issues listed.
- Use the QC hat tool to 'hatmap' your project, it must not have errors.

### Room Checklist

- Base files should be used for add_senses on groups of similar room types.
- Check a player's body position before attempting to move them.
- Check room and door exits to see that they work properly.
- Check rooms for proper light levels, outdoors, and terrain.
- Check that add_senses use variation ("rocks", "rock"), etcetera.
- Do not chain-load doors since it can cause an area to crash.
- If an object moves into a player's inventory it must recalculate weight.
- Indoor rooms need add_senses of ceiling, floor, and walls if appropriate.
- Mapenter rooms must be fully designed like any traditional room.
- Monsters must only reset if they are dead--do not use add_object to clone.
- Most mentions of a window should use the mudlib add_window feature.
- Outdoor rooms need add_senses of ground, dirt, grass, or relevant items.
- Players taking something from set_long need to then alter the description.
- Plural nouns must include add_items for the singular variant too.
- Room features (nouns) must have an associated add_senses to describe them.
- Room features must be interactive where relevant (chests, trees, etcetera).
- Rooms that spawn wandering monsters must have a no_clean_up property.
- Set the ranger and artificer terrain in outdoor rooms (excluding mapenter).
- Sort exits and doors going clockwise around a compass, starting with north.
- The set_long output must be at least 3 lines of text, and no more than 8.
- The set_outdoors must use room.h defines and not numeric values.
- Use ability checks wherever appropriate (climbing, searching, etcetera).
- Use add_message when possible instead of add_action or custom functions.
- Use force_followers when moving a player and it is logical to do so.
- Use the block_sit_messages and other related functions for interactivity.
- Water areas, such as creeks, rivers, ponds, and lakes must allow fishing.

### Monster Checklist

- All monsters must have a male or female gender except for animals/undead.
- Banish the names of monsters that you use in your projects.
- Check that monsters properly wear and wield their equipment.
- Do not use newlines in drama, except for tell_room/tell_object format none.
- Monsters must have at least 3 load_chat and 3 load_a_chat.
- Monsters that are level 17 and above must have some add_keyword speeches.
- The add_keyword speeches must only respond to players using 'say'.
- The load_a_chat should not mention weapons because they can be disarmed.
- The set_aim must use body_part.h defines and not numeric values.
- The set_name must be a lowercase, single word, without hyphens or slashes.
- The set_race should not be included in the set_alias too.
- The set_race has a maximum length of 15 characters, no exceptions.
- When using "guard" code you must have a check for rogues to sneak past.

### Object Checklist

- All objects (excluding invisible) must have 1 or more weight.
- Code objects as standalone files, rather than directly onto monsters.
- Mudlib gems cannot be saved into their own file, they must be cloned.
- The set_identify is required on special objects and with 500 or more value.
- The set_material is required on all types of objects.
- The set_smell, set_taste, and set_touch are required on all objects.

---

## SEE ALSO

- [qc](./qc/README.md)
