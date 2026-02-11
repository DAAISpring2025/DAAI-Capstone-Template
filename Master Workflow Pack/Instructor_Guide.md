# Master Weekly Autograding (Single Workflow) - Instructor Guide

This pack includes ONE GitHub Actions workflow that supports all 7 weeks.
You control the active week using `.github/week.txt`.

## Files included
- `.github/workflows/autograding.yml` (master workflow)
- `.github/week.txt` (set week number 1-7)

## How to set the active week
1. Open the TEMPLATE repository (the one marked as Template Repository).
2. Edit `.github/week.txt` and set it to the current week number (1-7).
   Example for Week 4: put `4` on the first line.
3. Commit the change.

## IMPORTANT: Protect the control file
In GitHub Classroom -> Assignment -> Grading and feedback -> Protected file paths, add:
- `.github/**`
This prevents students from changing `week.txt` or the workflow.

## How it works
- On every push, the workflow reads `.github/week.txt` to know which checks to run.
- Optional override: In GitHub -> Actions -> Run workflow, you can input a week number.

## Recommended weekly workflow (Instructor)
- Week 1: set week.txt to 1, create Week 1 assignment link
- Week 2: set week.txt to 2, create Week 2 assignment link
...
- Week 7: set week.txt to 7

## Tip
You can reuse the SAME assignment link if you prefer, but weekly separate assignments are cleaner for tracking.
If you reuse the same assignment, just update week.txt each week.
