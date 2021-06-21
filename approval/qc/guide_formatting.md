# SYNOPSIS

The formatting of a file is not just there for cosmetic reasons, it helps to
create a flow that makes things easier for reviewers to read through. If
everyone were to use their own style it slows down the review process because
it takes additional time and effort to readjust to every coder's unique
method. By having everyone do things similarly it streamlines the process
which means faster returns on your projects, and reduces the waiting time of
everyone else in line too. The guidelines below will help to reduce the width
and length of code, while improving consistancy between projects.

---

## DESCRIPTION

Wrapping: the game has a 77 character limit that must be adhered to. When
typing out something like an add_senses you must utilize all available
whitespace on each line until you reach the 77 character limit and then
perform a soft break over to the next line. Do not prematurely wrap, do not
exceed 77 characters per line, and do not hard break in the middle of a word.
Also, if you line up code on the left quotes it keeps the associated text
together which makes it easier to read.

Indenting/Braces: 2 space indents and condensed braces are the preferred
method. If you use the "tab" button on your keyboard you must also change
your editor's preferences to "replace tabs with spaces" or the equivalent
feature of your editor. This is necessary because tabs display with different
lengths for every program, while whitespaces are universal and consistant.

---

## EXAMPLE

```C
set_long("This rat is massive, and it stares at you intently with its sharp "
  "teeth, and long tail. The black, matted fur of its body shimmers "
  "occasionally in the light while it moves quickly about the room in a "
  "frantic manner.");

void some_function() {
  if(something) {
    do_something();
  } else {
    do_something_else();
  }
}
```

## SEE ALSO

- [qc](./README.md)
