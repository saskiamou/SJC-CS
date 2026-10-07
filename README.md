# SJC-CS-Group-Repo
COMPUTER SCIENCE CLUB: OUR FIRST SHARED PYTHON PROJECT

OUR GOAL
Each pair adds a small Python program to one shared GitHub project.
We review one another's work and combine our contributions.

1. CLONE OUR PROJECT

Replace CLUB-REPOSITORY-ADDRESS with the address from your organizer:

    git clone https://github.com/saskiamou/SJC-CS

Enter the folder it creates. Replace SJC-CS:

    cd SJC-CS

If you already cloned this exact repository, just enter its folder.

2. LABEL YOUR COMMITS

Inside this clone, use the details of the person making commits.
Replace the example text, keeping the quotation marks:

    git config user.name "Your Name"
    git config user.email "YOUR-COMMIT-EMAIL"

You can use your GitHub no-reply email from GitHub's email settings.
These settings label commits; they do not sign you into GitHub.

3. GET THE LATEST SHARED VERSION

Start with no unfinished edits from another task:

    git switch main
    git pull

If a command fails, ask the organizer before continuing.

4. MAKE YOUR PAIR'S BRANCH

    git switch -c [your-name]-feature

Run this once to create the branch.

5. EDIT YOUR PROGRAM

    nano [your-name].py

Type this into nano:

    name = input("What is your name? ")
    print("Hello, " + name + "! Welcome to our club.")

Save: Ctrl+O, then Enter.
Exit: Ctrl+X.

6. RUN YOUR PROGRAM

    python3 [your-name].py

Fix any problems in nano, save, and run it again.

7. CHECK AND SELECT YOUR CHANGES

    git status
    git diff
    git add [your-name].py
    git diff --staged

Status lists changed files.
Diff shows edits to files Git already tracks.
A new file appears in the staged diff after you add it.
Add selects the current version for the next commit.
If you edit again, run git add again.

8. SAVE YOUR COMMIT

    git commit -m "Add [your-name]'s changes"

The commit is saved on your Pi. It is not on GitHub yet.

9. PUSH YOUR BRANCH

    git push -u origin [your-name]-feature

Origin is the shared repository you cloned.
If access fails, ask the organizer. Keep credentials out of code.

10. REVIEW WITH ANOTHER PAIR

Open the repository on GitHub in a browser.
Choose Compare & pull request, or Pull requests > New pull request.
Choose your branch as the source and main as the destination.
Give the request a clear title and describe what you added.

Another pair reads your changes and watches your program run.
They leave feedback. If you need a fix, edit and run the program, then:

    git add [your-name].py
    git commit -m "Improve [your-name]'s program"
    git push

The new commit appears in the same pull request.

11. COMBINE AND SHARE OUR WORK

After review, the organizer or designated teammate merges the request.
Coordinate merges one at a time during the first lesson.

Once your work is committed and your contribution is merged:

    git switch main
    git pull --ff-only
    ls

Run a teammate's merged program:
Use python3 followed by that program's filename.

SUCCESS CHECKLIST
[ ] Our program runs.
[ ] We committed and pushed it.
[ ] Another pair reviewed it.
[ ] Our contribution was merged.
[ ] We pulled and ran a teammate's program.

IF YOU GET STUCK
Read the message, run git status, and ask the organizer.
Do not force-push or delete files to make an error disappear.
Use separate files for this first exercise.
Practice merge conflicts together in a later lesson.


OUR LONGER-TERM PROJECT: A CLUB TOOLKIT

WHY THIS PROJECT?
We can build useful tools for our own meetings.
Each pair can own a small part, and we can connect the parts later.

STAGE 1: SMALL, SEPARATE PROGRAMS
Choose one per pair:
- Meeting agenda: print today's activities.
- Quiz: ask a few questions and report a score.
- Idea picker: choose an activity from a list.
- Task checklist: display this meeting's jobs.

First milestone:
Every pair has one working program merged into the repository.

STAGE 2: CONNECT THE TOOLS
Learn functions and importing code from other files.
Build one menu that lets us choose which tool to run.
Agree on function names before connecting the programs.
Have one pair coordinate the menu while others improve their tools.

STAGE 3: REMEMBER INFORMATION
Save questions, ideas, and tasks in JSON or CSV files.
Load them when the program starts.
Handle missing files and unexpected input.
Keep sample data in Git instead of real personal information.

STAGE 4: IMPROVE AS A TEAM
Add tests for scoring and task handling.
Improve instructions and error messages.
Create GitHub issues for small features.
Use branches and pull requests to complete each feature.

STAGE 5: ADD RASPBERRY PI HARDWARE
Add a button to pick an activity, an LED to show status,
or a display for the agenda.
Keep the basic toolkit usable without hardware.
