# Contribution [#]: [Issue Title]

**Contribution Number:** [2]  
**Student:** [Alexandru Voicu]  
**Issue:** [https://github.com/Nebulyn-Labs/MediFlow/issues/408]  
**Status:** [Phase IV] [Completed]

---

## Why I Chose This Issue

[1-2 paragraphs explaining why this issue interests you, how it matches your skills/learning goals, what you hope to learn]
Second issue in the same repo I got my pull request approved. Continuing to work on this project and leveraging my experience in the code base.
---

## Understanding the Issue

### Problem Description
KPI cards are copy-pasted across several dashboard pages instead of using one shared component.
[In your own words, what's broken or missing?]

### Expected Behavior
One reusable KPI card component that takes props like title, value, icon, and color. All dashboards use it instead of their own copies. Looks the same as before.
[What should happen?]

### Current Behavior
Each dashboard page has its own separate KPI card code, so changes have to be made in multiple places.
[What actually happens?]

### Affected Components
Dashboard pages with KPI cards
New shared component/widgets folder
Existing KPI card styles (to merge into the new component)

[Which parts of the codebase are involved?]

---

## Reproduction Process

### Environment Setup

[Flutter web apps are easily tinkered with by opening in chrome through terminal. Setup environment is as easy as having flutter installed]

### Steps to Reproduce

This fix is less a bug that needs to be reproduced and more of a code cleanup - reformatting the way KPI cards are coded without any functional change

## Solution Approach

Similar to my original problem, the solution comes in the form of consolidating repeated code as it's own dart file within the repo that hosts a function which can be called back to within the rest of the project. In this problem, I need to create a dart file to build and design KPI cards, and then allow that to be accessed by any other file that original built them manually.

### Analysis

The KPI cards were created on the spot when needed originally, but as they were continuously used, the code began simply taking up space every time. Saving space by simplifying the process will help the codebase remain easy to read and upkeep.

### Proposed Solution

I'm going to create a class, KpiCard, with all the fields that would be needed to produce the original look of the MediFlow project while having enough variables to expand if ever needed. The helper widgets within the .dart file will be able to recreate the function of the original definitions while being significantly more simple in those files that used it than before.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [KPI card creation needs reusable code]

**Match:** [My previous fix included a very similar problem, Having to add a logout confirmation to every part of the codebase that interacted with logging out. To this end, I created a new file with a helper widget that was called in all files that logout.]

**Plan:** [Step-by-step implementation plan]
1. [Create kpi_card.dart and helper widgets to build the function]
2. [import kpi_card.dart into any file that defines KPI cards]
3. [Replace the original definitions with uses of the helper widget]

**Implement:** [https://github.com/iroquoispliskin2/MediFlow-avfork/tree/fix/dashboard-kpi-widget]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines? Yes]

**Evaluate:** [If I can implement my change and the site looks identical, It will be successful]

---

## Testing Strategy

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [10] Progress

[I had to run dart format . to ensure all checks on the PR would be passed. The maintainer said the change itself looked good, so now that I've added a proper description and ran dart flutter, it should be merged]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [https://github.com/Nebulyn-Labs/MediFlow/pull/469]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Approved]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
