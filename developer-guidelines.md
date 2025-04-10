# Developer Guidelines for Aspen Discovery

## Goals for Guidelines
* Make it easy to onboard new developers  
* Make the dev community as inclusive as possible  
* Distribute work as much as possible  
* Create the most stable software possible  
* Have a stable and sustainable developer community  
* Incremental updates to development workflows  
* Maintain a goal of feature improvement while not creating a workflow that inhibits progress
 
## Guidelines availability
Canonical version of the Aspen Community developer guidelines should be stored in a file named developer-guidelines.md in a repository dedicated to storing community guidelines. Content of the guidelines may be mirrored to [https://dev.aspendiscovery.org/](https://dev.aspendiscovery.org/)

The canonical version of this document will always be available at https://github.com/Aspen-Discovery/developer-handbook/blob/main/developer-guidelines.md

## Committing Code

### General Rules

#### Internal documentation
* All functions/methods should have documentation in the proper format for that language  
* All database fields should be commented with the field purpose

#### Atomic commits
* Make [atomic commits](http://en.wikipedia.org/wiki/Atomic_commit) of changes, even across multiple files, in logical units. That is, as much as possible, each commit should be focused on one specific purpose.  
* As much as possible, make sure a commit does not contain unnecessary whitespace changes. This can be checked with the command `git diff --check`
* If large amounts of formatting are necessary, the changes should be added to a whitespace-only commit.

### Commit Messages
As a general rule, your commit message should start with a single line that's no more than about 50 characters and that describes the commit concisely. If you feel the need for more detailed explanations, create a blank line, followed by a more detailed explanation.

For consistency, try to use the imperative present tense when creating a message. Examples:
* Use "Add tests for" instead of "I added tests for"  
* Use "Change x to y" instead of "Changed x to y"

When possible and applicable, commit messages should explain  
* What is changed  
* Why is it changed  
* How is it changed

For example, a typo fix answers these questions with the sentence  
`Fixed typo ‘teh’ to ‘the’ `
But a larger or more obscure change may require a paragraph or more explanation.

If possible, Add test plans to prove the patch does what it claims to do

In order to associate commits with GitHub Issues, the commit message should start with one and only one issue number and (optionally) a state change for the story. If the commit involves multiple issues, use the most specific issue possible.

### Message Template

Based on the [blog post](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) by [tbaggery](http://tbaggery.com/), here is a template to use as guideline for commit messages:

```
DIS-<ID> <optional state> (50 chars or so) Summary of change in imperative present tense

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. 

Further paragraphs come after blank lines.

- Bullet points are okay, too
- Typically a hyphen or asterisk is used for the bullet, preceded by a
single space, with blank lines in between, but conventions vary here

Test Plan:
1) lorum ipsem1
2) Blah blah
3) heyo
```

The issue id will typically be of the form DIS-X where X is an integer. The the future we may have separate Jira projects for sub-projects like aspen-docker and LiDA as needed.

## Merging

### Pull requests
When a branch is ready to be integrated into the “default” branch, the developer will make a pull request.

## Personal Data and GDPR

As Aspen is used internationally, GDPR should be taken into consideration. GDPR is in place across Europe and is a set of data protection rules. It limits what organizations can do with personal data. 

### Personal Data

Any piece of information that relates to an identified or identifiable individual. 

### Personal Data in Aspen

Where new developments require the processing and / or storage of Personal Data, there are a few steps developers should take to ensure GDPR compliance:

* Consider whether the personal data needs to be stored in Aspen or whether it can be stored in the LMS.  
* Consider how long this data needs to be stored and update the DatabaseCleanUp.java script to ensure the personal data is removed or anonymized at the earliest opportunity.

## Managing Issue Assignment
* Don't reassign issues without the consent of the current assignee
* If no response is made in a reasonable time frame ( 1 week for non-critical issues, 48 hours for critical issues ), issues may be reassigned without consent

## Releaseing

# Release candidates
* 10 days Prior to release, a releease candidate ( e.g. 24.12.00-rc.1 ) will be tagged
* If commits are added to the branch of that tagged release, a new release candidate ( e.g. 24.12.00-rc.2 ) will be tagged at the end of the day
 
## TBD: Aspen Community Code of Conduct
A document that establishes expectations regarding the behavior of contributors and participants.  It often helps communities to build a positive social atmosphere.   
Key points that should be covered:
* Where the conduct takes place e.g. pull requests, community events etc  
* Who the code applies to e.g. sponsors, maintainers etc  
* Consequences of violations  
* How to report violations

Two community code of conduct examples:
* [Koha Community Code of Conduct](https://koha-community.org/about/policy/code-of-conduct/)   
* [Atom](https://github.com/atom/atom/blob/master/CODE_OF_CONDUCT.md)  

When a code of conduct is adopted, this section will be updated.
