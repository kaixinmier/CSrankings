# Contributing to CSrankings

Thanks for contributing to CSrankings! Please read **all** these guidelines to getting your pull request accepted. **IF YOU DO NOT DO THIS, YOUR COMMIT WILL BE SUMMARILY REJECTED.**

1. Use a reasonable title that explains what the PR corresponds to (as in, not "Update csrankings-x.csv").

1. Do not modify any files except `csrankings-[a-z].csv` or (if needed) `country-info.csv`.

1. _Do not use Excel to edit any .csv files; Excel incorrectly tries to
convert some Google Scholar entries to formulas, corrupting the
database. Use a text editor like emacs or NotePad instead._

1. Check to make sure that you have no spaces after commas, or any missing fields.

1. Check to make sure the home page is correct.

1. Make sure the Google Scholar IDs are just the alphanumeric identifier (not a URL or with `&hl=en`).

1. Check to make sure the name corresponds to the DBLP entry (look it up at http://dblp.org).

1. If a faculty member is not in a CS department or similar, include a comment explaining how they meet the inclusion criteria (see below).

1. _Insert new faculty **in alphabetical order**, not at the end of `csrankings-[a-z].csv`._ **Do not modify `csrankings.csv`, which is auto-generated.**

1. _When submitting the PR request, make sure to read and check **all** the boxes in the PR template below by filling them in with an X._ Do not update the file `CONTRIBUTING.md` in your commit, only in the PR. **IF YOU DO NOT DO THIS, YOUR COMMIT MAY BE SUMMARILY REJECTED.**

**Inclusion criteria**

- [ ] Make sure that any faculty you add meet the inclusion
criteria. Eligible faculty include only full-time, tenure-track research
faculty members on a given campus who can *solely* advise PhD students in
Computer Science. Faculty not in a CS department or similar who can
advise PhD students in CS can be included regardless of their home
department. Faculty should also have a 75%+ time appointment (check
`old/industry.csv` for faculty who are now more than 25% in industry).

**Updating an affiliation or home page**

- [ ] Update affiliations, home pages, and Google Scholar entries by modifying `csrankings-[a-z].csv`. For the Google Scholar entry, just use the alphanumeric identifier in the middle of the URL. If none is there, put NOSCHOLARPAGE.

**Adding one or more faculty members (including an entire department)**

- [ ] If the department is not yet listed in CSrankings, the entire faculty needs to be added (not just one faculty member).

- [ ] Enter each faculty member's [DBLP](http://dblp.org) name, home page, and Google Scholar entry (just the alphanumeric identifier, not the whole URL) by modifying `csrankings-[a-z].csv` (**the letters correspond to the first letter of the faculty members' names**); include disambiguation suffixes like 0001 as needed. If the faculty entry is currently ambiguous, please do not include them. Send mail to the DBLP maintainers (dblp@dagstuhl.de) with a few publications by a particular faculty member; also, open an issue so that when the DBLP database is updated, that faculty member's information can be added.

- [ ] If DBLP has multiple entries for this person, all of them need to be listed. Do not update `dblp-aliases.csv`.

- [ ] If the institution you are adding is not in the US,
update `country-info.csv`.

**(Advanced) Quick contribution via a shallow clone** 

A full clone of the CSrankings repository is almost 2GB.  To contribute a change without creating a full local clone of the CSrankings repo, you can do a _shallow clone_.  To do so, follow these steps:

1. Fork the CSrankings repo.  If you have an existing fork, but it is not up to date with the main repository, this technique may not work.  If necessary, delete and re-create your fork to get it up to date.  (Do **not** delete your existing fork if it has unmerged changes you want to preserve!)
2. Do a shallow clone of your fork: `git clone --depth 1 https://github.com/yourusername/CSrankings`.  This will only download the most recent commit, not the full git history.
3. Make your changes on a branch, push them to your clone, and create a pull request on GitHub as usual.

If you want to do another contribution and some time has passed, perform steps 1-3 again, creating a fresh fork and shallow clone.


