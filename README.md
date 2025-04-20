<img width=300 align=left src='docs/undraw_project_completed.svg'>
<div>

### <samp>Pastel

**Pastel** is an open-source, self-organizer task list CLI program
I'm planning and making myself, and for myself use. All features
and use cases are made based on my personal use and needs.

I really encourage you not using this app, instead
learn the code and make your own.
</div>

<br>
<div align=center>

![Linux support](https://img.shields.io/badge/Linux-%23.svg?style=for-the-badge&logo=linux&logoColor=2f2e41&label=support&labelColor=00bfa6&color=f1f1f1)
</div>

<br>
<br>
<br>
<div align=right>

# <samp>Usage
</div>

```sh
$ todo                         # List all tasks
$ todo add 'task' 'description' ... 'task'
$ todo rm 'index'...
$ todo done 'index'...
$ todo sort                    # Order todos by state
$ todo cal                     # Show calendar

$ todo note                    # Show notes in group '' (global group)
$ todo note 'group'            # Show notes in group
$ todo note add 'note'... 'group'
$ todo note rm 'index'... 'group'

$ todo todo                    # List todos
$ todo todo add 'todo' 'description' ... 'todo'
$ todo todo rm 'index'...
$ todo todo done 'index'...    # Turn todo into done task
```

For todos management the indexes in the today's list is used.  
It seems to help the interface's development since no technical info need to be available (i.e. UUID).

Tasks have a date and state, and become unchangeable once the day passes. In contrast,
todos don’t have a date—when marked as done, they turn into a completed task for the current day.

Multiline support is not giving directly, but through the shell when enter is pressed with an open quote.
