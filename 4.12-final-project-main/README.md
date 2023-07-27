# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Building a Social Media Clone


We're almost done! 

Our last project is going to be a group effort. Everyone in the class is going
to be working together to create a social media clone using React for the front-end
and Django and PostgreSQL for the back-end. 

Much like the previous group project, one of the most challenging aspects of
this will be communication and coordination. Do you best to be the kind of
collaborator you'd like to work with!

What you need to do for each other:
* Communicate in a way that is **A**ctionable, **S**pecific, and
**K**ind.
* Clearly communication your expectations of your teammates
* Ask for help when you need it
* Offer help when you think others may need it

## Requirements

### Planning

* Have a thoroughly documented Team Expectations Google document.
* Have a thoroughly developed, beautiful [README.md](https://git.generalassemb.ly/sei-axolotls/documentation-markdown) file.
* Take time for each team member to discuss where they feel strongest and weakest, in terms of coding ability.

### Collaboration

- Every team member must have roughly the same number of individual commits in
  the commit history for your app (dividing responsibilities between different
  parts of the app is fine, but every team member must have commits in the
  project).
- Every team must follow the ["Feature Branch" Git workflow](https://bocoup.com/blog/git-workflow-walkthrough-feature-branches).
- Every team member must speak for roughly the same amount of time during the group presentation.
- Every team member should have a solid understanding of the *entire*
project (Even the features implemented by other team members).


### Back-End Requirements

- Your back-end must be a Python, Django, and PostgreSQL API with authenticated
 users, posts, and comments.
- Must have Create, Read, Update, and Delete functionality built throughout the
  app (i.e. You don't need full CRUD on every model, just full CRUD throughout
  your models where it makes sense).

### Front-End Requirements

- Your front-end must use React.
- Your application should include at least five reusable components.
- You must use React Router to handle multiple views.
- You must communicate with the back-end API RESTfully to Create, Read, Update,
  and Delete resources (using either `fetch` or `axios`).
- Your application will be styled with CSS and have a responsive design for at
least two screen sizes.

### Housekeeping

- Indent properly.
- Use semantic variable names.
- Follow proper case conventions (`camelCase`, `kebab-case`, etc).
- Remove unnecessary boilerplate React files and code.
- Remove all `console.log()`s and commented out code (functional notes/comments
are okay).

### Deployment

- Your API must be deployed to Heroku and your front end must be deployed to
  GitHub pages, Surge or Netlify. Applications that are not deployed will be considered
  incomplete.

## Submission

Your work will be done using your personal github accounts in the
[SEI-Embers](https://github.com/orgs/SEI-Embers/) organization! A (blank)
 project repo has already been created for you but you can, of course,
change the name of it once you decide on what to call your clone. 

# GETTING STARTED

## STEP 0. Get Your Design Approved

Have a professional mockup ready to present to instructors for approval so that your team can proceed to next steps.

## STEP 1. Read All Instructions

Yes, there's a lot here, but this was created with multiple generations of cohort and instructor input and contains instructions and tips that **will** make your project week easier. If you do not follow the instructions and consequently require assistance for an avoidable issue, we'll have to get out the shame bell.

![shame bell](https://thumbs.gfycat.com/VillainousCheapIndianelephant-max-1mb.gif).

<br>

## STEP 2. Set Team Expectations

Your group should take at least 30 minutes to create a team expectations document. This should include:

1. **Timeline:** An overview of every day and when you will be hacking with your team.
2. **Teammates:** Who's on the team, and your personal strengths and weaknesses.
3. **Team Values:** Communication preferences, goals, values.
4. **Team Practices:** Naming conventions, git branching practices, express routes.

> [Team Expectation Setting Template](https://docs.google.com/document/d/1TuvOuy0UQ42KGOza9IAGs8pkPfmoIlVP4Vj6OnJNGG4/edit?usp=sharing)

<br>

## STEP 3. Scope the design

**Your team must have the following items written up in the repository's `README.md` file to get approved.** 

1. **Schema**: Please have your schema(s) ready to show the instructors. Schemas drive the project.
1.  **Whimsical Flowchart**: A link to the whimsical flowchart to convey the data flow between your front-end and back-end, with component hierarchy included (remember to enable public link access)
2. **Team Expectations**: A link to your team's Google document that establishes timelines, communication preferences, code conventions, git practices, etc.
3. **Overview:** 4 to 5 non-technical sentences, summarizing the features, functions, and goals.
4. **MVP:** A link to your [GitHub Projects](https://github.com/features/project-management) board (See Step 5)

<br>

## STEP 4. Project Management

- Create either a [GitHub Projects](https://github.com/features/project-management) or [Trello](https://trello.com/) board on your repo to prioritize and assign tasks. Common categories include `to do`, `in progress`, `done`, and/or `new`, `now`, `next`, and `later`.




- Each group member should choose or be assigned tasks during standups.
- Break features into small, focused tasks. If a task can be made more granular, create a new task card on the project board describing the sub-tasks.
> We'll have a standup in the morning where we figure out who's going to be
working on what and share what blockers, if any, people are facing with their
current tasks. We'll have another standup at the end of the day to go over
progress and blockers and make adjustments as necessary.

>Standups should be quick. Each person is going to share just enough so that
everyone knows what's going on. If you need to talk about a particular blocker
in detail, that'll happen after the standup is done.

- Work on a feature branch. Naming convention is [INITIALS]-[FEATURE] ie.
  ```cd-nav-bar```
- COMMIT AND PUSH YOUR FEATURE BRANCH OFTEN. 

- Once you've finished work on a feature, submit a pull request. In the comment
for your pull request, reference the issue that your request is for. 
- After the pull request is made, the code needs to be reviewed. Select the Git
Czar as a
reviewer on github, then send the Git Czar a slack with the message "PR" and a link to
the pull request.
- If all is good, I'll approve and merge it. If there's more work that needs to
be done, I'll add a comment and send it back to you. 
- Once a change is merged, I'll send a message to all y'all on slack that a new
pull request has been merged. When you see that, you should pull down the
changes and merge the changes to he main branch into your feature branch.

<br>


## Necessary Deliverables

Your submission must include **all** of the following:

### Project Idea and Initial Planning

By the end of Day 1 of this project, you need to submit an issue to this repository:

1. Your project name!
2. A list of your models and their properties

These can be submitted in an issue on **this repository**.

### Final Application

Your project is due on the last day of the project. 

Your back end API should include:

- A working JSON API (built by your team) built using Django that
  meets the technical requirements above.
- Frequent commits dating back to the very beginning of the project.
- A link to your hosted, working API. 

The front end of your application should include:

- A working front end application  built with React, React
  Router, utilizing a Component Library (built by your team).
- Frequent commits dating back to the very beginning of the project.
- A link to your hosted, working application.

Your documentation should include:
- A `readme.md` file in the root of your repo that follows
  [good standards of documentation](https://git.generalassemb.ly/sei-axolotls/documentation-markdown)
  (i.e. explanations of the technologies used, the approach taken, features,
  installation instructions, unsolved problems, etc.)
- A `planning/` directory in the root of your repo containing a diagram mapping
  out your project domain. You are welcome to include other planning documents
  (e.g., wireframes, user stories).


## Contribution Guidelines

- Each member of your group **_must have an individual commit history_** to your
  project's repositories (Multiple commits per group member).
- Each member of your group is expected to present for an equal amount of time
  during [project presentations](presentations.md), which last at least 10
  minutes per group.


## Tips 

### Process

- **Write pseudocode** before you write actual code. Thinking through the logic
  first helps.
- **Write tests** that translate your pseudocode into requirements for the code
  you need to write. Then, write just enough code to make your tests pass!
- Don't hesitate to **write throwaway code** to solve short-term problems.
- **Read the docs** for whatever technologies / frameworks / API's you plan to
  use. (See ["RTFM"](https://en.wikipedia.org/wiki/RTFM))
- **Continuously Deploy** your code. Like, deploy at least once a day - ideally
  twice a day.
- **Work Together**. Sometimes just explaining the situation to another person (or rubber duck)
is enough to get you "unstuck" on a problem. 

### Code

- **Keep your code DRY** and build your APIs RESTful.
- **Be consistent** with your code style. You're working in teams, but you're
  only making one app per team. Make sure it looks like a unified effort.
- **Commit early; commit often.** Don't be afraid to break something because you
  can always go back in time to a previous version (so long as you're committing
  often).
- **Deploy early; deploy often.** Deploy your work as early as possible, even if
  you don't really have anything completed. Heroku issues **always** pop up.
  Don't be caught short just before the submission deadline!
- **Name things appropriately. Comment as necessary.** Do your naming
  conventions make sense? Would another developer be able to look at your app
  and understand what everything is? (See
  ["self-documenting"](https://en.wikipedia.org/wiki/Self-documenting) and
  [Code Tells you How, Comments Tell you Why](https://blog.codinghorror.com/code-tells-you-how-comments-tell-you-why/)).
  Even if it's obvious, comments can help to explain the intent -- the what and
  why. This allows the next developer to understand the purpose and decide what
  can be adjusted to achieve the same goal.
- **Ensure it is well-formatted.** Are you indenting consistently? Can we find
  the start and end of every div, curly brace, etc? Organizing the hierarchy is
  key to understanding.

Teams of developers usually adhere to an agreed-upon set of code-style rules.
This reduces issues with reading our colleagues' code. We strongly recommend
using [StandardJS linting](https://github.com/standard/standard#install) or
[PrettierJS](https://github.com/prettier/prettier).

## Resources

- [HackDesign](https://hackdesign.org/lessons) (beginner's reference for
  thinking like a designer)
- [UX Design for Developers](https://hackernoon.com/ux-design-for-developers-d3429200a1da)

## Plagiarism

Take a moment to re-familiarize yourself with the
[plagiarism policy](https://git.generalassemb.ly/DC-WDI/Administrative/blob/master/plagiarism.md),
specifically on using work you find online and on work you do with other
students.

We give assignments like this to give you the opportunity to review the material
in class in a practical manner. By building something using what you've learned
in class, you'll be reviewing the material and gaining a deeper understanding of
it.

These assignments are similar to those you can expect when applying for a job,
either in the form of a take-home coding challenge or an in-person technical
interview. So it's important that you put in your best effort now and challenge
yourself to do this assignment on your own.

If you are struggling with the material, that's alright! That's why you're here.
First, try reviewing the previous lessons and exercises. Go easy on yourself,
you're still learning! If you're still struggling after that, come to office
hours and ask an instructor for help. They're here to help you!

Don't copy and paste from another source or another student or the solution
branch. That's just going to put you at a disadvantage when you're interviewing
for a job
