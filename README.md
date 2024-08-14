<img width=300 align=left src='docs/undraw_project_completed_re_jr7u.svg'>
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

# <samp> Main features
</div>

- Week names and description
- Simple and lightweight


<br>
<br>
<br>
<div align=right>

# <samp>Usage
</div>

I'll probably not add a man page, nor a help page.  
But something futurally to help the usage of it generally.

```sh
$ pastel add "Some task for today next fiting hour"
$ pastel add note "Some note for right now"
$ pastel done                                       # Mask done task that fits now time
$ pastel done 3                                     # Mark done task with index 3 today
```

For task/note management it's used the index of it in the today's list.  
It seems help the interface's development since no technical info need to be available (database UUID).


<br>
<br>
<br>
<div align=right>

# <samp>Interface
</div>

```
                 My good week 🪴
          This is the week's description
          that is to remember how I want
             it to be during the days
      ╭
      │○ Take a shower                            All day tasks
      │● Water plants
      │○ Give myself some sunshine
      │    I've needing more D-vitamine
      │    At least I guess so, I'm wetto asf
      │
      │● Buy chips
      │
      │
11:00 ○ Scriptures Study                          Undone task
11:15 │
      │
12:00 ● Lunch                                     Done task
      │
12:15 ├ It's a note I took in the afternoon       Note
      │ after noticing I needed to take a
      │ note about what happened today
      │
13:00 ○ Math Study
      │   Some description for my math class      Task description
      │   this is a course I purchased yey
      │
15:00 ✖ Portuguese Study                          Canceled task
      │-  The teacher canceled for some illness
      │
      ╰
```

More updated and precise information can be found at [`docs/interface.txt`](docs/interface.txt).  
And the colored interface at [`docs/interface-colors.sh`](docs/interface-colors.sh).


<br>
<br>
<br>
<div align=right>

# <samp>Database
</div>

No database to use was decided yet.  
I don't know how I'm going to organizate it yet.

<br>

Task model:
- Title
- Description
- State
	- Done
	- Canceled -- It's required a reason to cancel
- Date
- Time -- Null if all day
	- Start
	- Finish
- Repeatition
	- Today
	- Today-Stack -- If undone today, move to tomorrow
	- Daily
	- Weekly
	- Monthly
	- Annually
	- Every weekday

Node model:
- Content
- Date
- Time -- Null if all day
	- Start
	- Finish
