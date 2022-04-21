# Task Management

**Objectives**

- Describe the high-level structure and organization of a research program.
- Identify different kinds of development processes in a research project settings: Agile and Sturdy Developments
- Employ an issue-tracking system such as kanban to organize project tasks and deliverables, e.g. Asana, Trello, Confluence

This arc of the class focuses less on the code products structuring the details of your research and more on the strategic and instrumental capabilities you can build to support your work.  To the extent we use code, it's less about new concepts and more about outfitting your toolchain.

- Task Management
- Workflows & Lifecycles
- Testing & Integration
- Reproducibility
- Authorship & Publishing
- Collaboration
- Licensing & Legal Issues

We also want your input on these discussions, since several of these are more qualitative in nature.

We are also introducing the term project for the course now.  Essentially, we want you to take a current or new research project or effort you've made and apply the things you've learned in this class.

You'll need to start off by deciding by April 10 what your project will include.  Over the next few weeks, you'll apply the principles of the course to realizing as much of it as you can in that timeframe.  In May, you'll present a 10–15 minute discussion of how you applied the principles of this course to your research question and analysis.

- [Project Proposal](https://canvas.illinois.edu/courses/16488/assignments/423466), due 4/10
- Project Review Time on 4/20
- Final Presentations on 5/2 and 5/4

---

To prime the pump for our discussion today:

- What are the top three items on your research project's to-do list?  (If you don't have a research project, think of another project.)


## Project Management

The goal of project management is to coordinate effort and attention efficaciously.  Let us define a _project_ as a structured set of tasks with an objective goal and deliverable at the end.  (The structure of tasks may not be well-defined in advance; think about something huge like the Manhattan Project.)

A project may involve one to many people.  Just because you are working alone on a project doesn't mean that you should ignore the structure of your attention, although many collaborative elements may not apply.

### Elements of Projects

For most projects, a _post hoc_ analysis would show something very similar to this (nonsequential) outline:

1. Inputs
    1. Data sets
    2. Observations
    3. Experiments
    4. Models:  mathematics & physics
2. Analysis
    1. Experiments
    2. Code ("_in silico_")
    3. Mathematical & physical modeling
    4. Verification & validation
3. Outputs
    1. Deliverables:  products, software, patents, papers, visualization
    2. Predictions

A large project may fractally contain this cycle writ small for many tasks.  You need to be able to juggle the demands of each of these without losing the thread of your work.  **Whatever non/system you use, you shouldn't rely on memory.**

+Feynman

Today we'll cover some project management and some task management.  The question of deliverables and wrapping all of this up into a single project will be covered next time in Workflows & Lifecycles.

- [_NASA Systems Engineering Handbook_](https://www.nasa.gov/sites/default/files/atoms/files/nasa_systems_engineering_handbook.pdf)

- [_Systems Engineering Body of Knowledge_](https://sebokwiki.org/wiki/Guide_to_the_Systems_Engineering_Body_of_Knowledge_%28SEBoK%29)

### Project Management Schemes

Project management is a highly theoretically-structured discipline.  Big business, operations research, capital investors, and other stakeholders have been highly motivated to develop PM along very formal lines.  We aren't going to delve deeply into most of these, but rest assured they are out there.

For most projects at the scale of an academic research project, lean project management suffices.  "Lean" refers to minimization of formal distractions and time sinks.  One of the most popular schemata has been the Agile method, and many simple derivatives exist and are used even in small software teams.

#### Agile Practices

> In software development,agile practices involve discovering requirements and developing solutions through the collaborative effort of self-organizing and cross-functional teams and their customer(s)/end user(s).

In other words, rather than lay out the entire project structure at the beginning (as some traditional techniques prefer), agile development prioritizes regular check-ins with the "customer" and re-orientation towards evolving goals.  The "customers" in our case are you, your advisor, editorial reviewers, users of your research software, and so forth.

There's an "Agile Manifesto" (of course!), and it's worth taking a glance at their principles:

1. Customer satisfaction by early and continuous delivery of valuable software.
2. Welcome changing requirements, even in late development.
3. Deliver working software frequently (weeks rather than months)
4. Close, daily cooperation between business people and developers
5. Projects are built around motivated individuals, who should be trusted
6. Face-to-face conversation is the best form of communication (co-location)
7. Working software is the primary measure of progress
8. Sustainable development, able to maintain a constant pace
9. Continuous attention to technical excellence and good design
10. Simplicity—the art of maximizing the amount of work not done—is essential
11. Best architectures, requirements, and designs emerge from self-organizing teams
12. Regularly, the team reflects on how to become more effective, and adjusts accordingly

One of the most characteristic practices of agile development is the use of a "daily stand-up," a meeting where everyone reports on the previous day's work, everyone discusses their own next steps, and impediments to progress are discussed.  (This is a very healthy practice for an active research project, and can be implemented by yourself too.)

There is heavy use of software automation to take care of repetitive human tasks and needs, such as automatic testing, test-driven development, and issue and task tracking.

A couple of criticisms should be made of standard agile practices:

1. Agile doesn't call for careful code planning and documentation.  Your project should have some of both of these.  As you aren't a trained software developer, you should take some time before you embark on a large project, perhaps consulting with a colleague, and chart the big picture before you begin the daily agile cycle.
2. Agile places a fairly high onus on future-you to make good decisions around managing tasks.  If you know that you typically have trouble deciding or planning under certain circumstances, you should avoid your agile planning session at those times.  (Work with your mental processes, not against them.)  Task management can help with this.

- [Managing Research Software Projects:  Agile Development](https://swcarpentry.github.io/managing-research-software-projects/15-agile/)
- ["Agile Software Development", Wikipedia](https://en.wikipedia.org/wiki/Agile_software_development)

* Include Automation section from the last lesson here.


## Task Management

One of the most critical components of an effective research program is capturing and executing on tasks.  Tasks can arise systematically (from known requirements) or emergently (as a situation develops in new and unforeseen ways).

- What is a task?  (A discrete step with a deliverable.)

An “issue” isn't quite the same thing as a task, in our parlance, but we can use issue management systems like GitHub's to track some kinds of tasks.

One of the simplest task management systems is [_Getting Things Done_](https://lifehacker.com/productivity-101-a-primer-to-the-getting-things-done-1551880955).

1. Capture everything.  To-dos, ideas, recurring tasks, responsibilities, etc.
2. Clarify things you have to do.  Be specific with actionable steps.
3. Organize actionable items by category and priority.
4. Reflect on your to-do list.  Do short things right away, and break down vague steps further.
5. Engage and get to work.  Choose the next action and go.

Also take a look at [Bullet Journaling](https://lifehacker.com/the-bullet-journal-productivity-method-empowers-your-pa-1169313228).  I went through a phase of using complex online systems like del.icio.us (way back in the day!) and Evernote.  However, I've come to believe that services like these are largely unreliable.  In practice, I use four overlapping systems depending on context:  a series of text files, Obsidian, GitHub kanban, and a physical notebook or clip of cards.

### Gumption Traps

Some tasks are _blocking_, meaning that effectively nothing can proceed until they are completed satisfactorily; these are frequently precisely the tasks that we procrastinate.

Robert Pirsig refers to these procrastinated tasks as "gumption traps":

> There’s another kind of detail that no shop manual goes into but that is common to all machines and can be given here. This is the detail of the Quality relationship, the gumption relationship, between the machine and the mechanic, which is just as intricate as the machine itself. Throughout the process of fixing the machine things always come up, low-quality things, from a dusted knuckle to an accidentally ruined "irreplaceable" assembly. These drain off gumption, destroy enthusiasm and leave you so discouraged you want to forget the whole business. (Robert Pirsig, _Zen and the Art of Motorcycle Maintenance_)

- Exogenous gumption traps are "setbacks," or outside conditions like a poorly understood system or documentation, or inadequate tooling.
- Endogenous gumption traps are "hang-ups," such as mindset, impatience, and overwhelm.

One critical purpose of a good task tracking system is for you to be able to identify and confront the gumption traps.  Of course, you won't do that all the time right away—but at least you will know what they are and be able to look them square in the eye.

> It's natural to feel fear of code; however, you must act as though you are able to master and change any part of it. To code courageously is to walk into any abyss, bring light, and make it right. (Philip Monk)

The trouble with a blocking task is that it invites you to _bikeshed_, or work on cosmetic and easily-comprehended portions of your task list that don't aid your forward momentum.  (There is a place for a bit of cathartic relaxation, to be sure, though.)

One of the worst situations occurs when a high-priority task is blocked by a low-priority task.  Imagine trying to model a surface reaction on a small computing cluster (the big picture) but having a persistent minor bug of some atoms simply disappearing at the boundaries between CPU domains (a small task).  Of course, the solution is for the low-priority task to assume the same priority level as the high-priority task it blocks, but to do so requires us to actively face the situation.

### Issue Tracking

Issue tracking is an attention-surplus technology.  You have to use the tool, whatever you adopt, and you have to check it regularly to stay on task.

Basic issue tracking requires you to maintain a list of next steps for your project.  You can categorize these as `minor`, `critical`, `easy`, `wishlist`, and so forth.  These may be done on paper or with Post-It notes (as with kanban, below).

- [Robin, “Style guide for issue tagging”](https://robinpowered.com/blog/best-practice-system-for-organizing-and-tagging-github-issues)

Issues proceed through a well-defined lifecycle of their own.

![](https://swcarpentry.github.io/managing-research-software-projects/fig/issue-lifecycle.png)

One simple solution is to use the GitHub issue tracker.  While originally instrumented for filing bugs and tracking fixes, issue tracking has become a solid way to embody future intent.

For single-person research projects, anything other than priority is probably too much to manage.  What I do in practice:  I have a clip of index cards divided by location (_not_ project).  Whenever I go to a new place, I check the card and see what there is to do.  Essentially the idea is to exclude the role of memory in keeping track of what I need to do.

### Kanban

A kanban board formalizes the stages of task tracking.  Each task is given a card, and each card starts at the left-hand side of the board as task-in-waiting.  As progress is made, the task proceeds to the right until it is complete.  Several tasks may be in any category at any given time.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Kanban_board_example.jpg/581px-Kanban_board_example.jpg)

Constraint of workflow is one of the key rules for kanban.  Typically, no more than five tasks can be worked on by the team at a time; for a single researcher, this number should probably be a bit lower.  Items may have sub-items, tags, etc.

(I have used kanban successfully for well-structured projects that I need to coordinate with others, like producing a paper or a presentation.  The biggest problem is training others to actually use the system.)

- [Managing Research Software Projects:  Issue Trackers](https://swcarpentry.github.io/managing-research-software-projects/08-issues/)


## Discussion Points

- What states should your project issues be allowed?  (Alternatively, what columns on the kanban board?)
- What tools have you used to track and manage tasks?
