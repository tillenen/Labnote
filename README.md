Lab Note
========

Laboratory notebook of lab 404, Department of Molecular biophysics, Bogomoletz Institute of Physiology.

Property of I, A & B.


## Structure of lab notes
In this notebook using Markdown markup for text notes and CSV sheets format for storing reagents compositions. I recommend that you store all updates in reagents and protocols folders in `master` branch and personal project records in separate branch (e.g. `researcher_name` branch). And separate branches require independent repositories in local machine. 


There are three main directories:
 1. Projects
 2. Protocols
 3. Reagents


## Projects
Contain individual directories for each project.
Each project folders must have unique tag and year in name and contain head file with detail description of project and individual folders for daily notes and results files.

## Protocols
Descriptions of standard protocols for laboratory manipulations. Presence of detailed protocol will simplify writing of future work notes (just insert reference to standard protocol).

## Reagents
Composition of solutions and reagents.
Data storing in CSV table format and have next columns:
 - Chemical - name of chemical
 - ID - manufacturer and serial number
 - MW (g/mol) - molecular weight
 - Stock Solution - concentration of srock solution (if you don't use SS just mark as "solid")
 - Concentration - final concentration
 - volume - mass or volume of stock solution for the specified solution volume (there may be several "volume" columns for different final solution volumes)

---

#### GitHub cheatsheet

Main **git** commands that you may needed for work are present below, enjoy. But first you should create fork of Labnote repo on your GitHub account.


- Clone `master` from GitHub repo: `git clone https://github.com/wisstock/Labnote.git`
- Clone repo for personal use `git clone Labnote Labnote_researcher_name`
- Create personal branch and switch to it: `git branch researcher_name`
- Create new `git remote` for you cloned repo:
```
git remote add personal_remote https://github.com/user_name/Labnote.git
```

&nbsp;

- For editing reagents or protocols go to **Labnote** folder and switch to `master` branch: `git checkout master`
- For saving changes in Reagents or Protocols folder in `master` branch follow next steps (**Warning: DO NOT use master branch or Labnote repo for personal records, for Reagents and/or Protocols only!**):
```
git add --all
git commit -m "commit message"
git push origin master
```

- For sync your **Labnote** repo with upstream `master`:
```
git remote add upstream https://github.com/wisstock/Labnote.git
git fetch upstream
```

&nbsp;

- For editing projects records go to **Labnote_researcher_name** and switch to `researcher_name` branch:
```
git checkout researcher_name
git remote set-url origin https://github.com/user_name/Labnote.git

```

- For pushing projects records to GitHub repo branch:
`git push -u origin researcher_name`

- For saving changes in projects records follow next steps:
```
git add --all
git commit -m "commit message"
git puch personal_remote researcher_name
```
- Sync you personal repo **Labnote_researcher_name** with update of Reagents and Protocols from `master` branch:
```
git merge master
```