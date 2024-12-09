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

For consistency, try and use the imperative present tense when creating a message. Examples:
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

In order to associate commits with GitHub Issues, the commit message should indicate one or more issue number and (optionally) a state change for the story. The commit message should start with square brackets containing a hash mark followed by the issue number. For example:

### Message Template

Based on the [blog post](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) by [tbaggery](http://tbaggery.com/), here is a template to use as guideline for commit messages:

```
#issueid <optional state> (50 chars or so) summary of changes

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
