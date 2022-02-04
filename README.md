# Harvest data

_Please setup a Git repository on GitHub / GitLab / wherever, and do regular commits to show your progression, then share a link to your repository with the interviewer when finished. If you're unfamiliar with Git, email your solution back instead._

It’s harvest time. We have a feed of harvest data from a data supplier. They supply us a file which will be updated throughout the month as harvest data comes in.

## Data processing

Data files are found in the folder `csv files`:

- `harvest data – clean.csv` (use this for the first part of the exercise)
- `harvest data – validation needed.csv` (use this for the “validation” part of the exercise)
- `override.csv` (use this for the “Override” part of the exercise)

### Output a standard result

The fields in the file will be separated by commas but each row will vary in length as described below.

A result will consist of:

1. A County
1. A repeating set of pairs, containing a crop code & weight harvested (in tonnes)

So for example:

```
Cambridgeshire, W, 212, PO, 873, O, 72
Suffolk, PA, 28, M, 872, W, 782, BE, 213
```

Transform this into a standard result that shows:

- the County
- translates the crop code into the full name of a crop
- shows the weight as a percentage of all crops harvested in that County 


#### Crop codes

- W - Wheat
- B - Barley
- M - Maize
- BE - Beetroot
- C - Carrot
- PO - Potatoes
- PA - Parsnips
- O – Oats

### Validation

If there is a problem with the format of the data file then all good entries should result in output and the error should go to a separate error log with the problem explained in non-technical language that a farmer might be able to understand and report back to the data service.

### Override

The data service may be behind the actual harvest data or may contain an error. We want to be able to combine the data file with an "override" file. If a County has an entry for a crop in the override file that value should be used instead of the original data file.
If the crop is not present in the original data file the result should be added entirely from the override file.

## Login webpage

Make a non-functional (i.e. not integrated with any Java/PHP code, only HTML / CSS) webpage template, which will eventually be used to login to a Harvest Data website. Feel free to use any front-end framework (Bootstrap, Zurb etc), or vanilla CSS, the choice is open.
It should have the following features:

- The NIAB Logo (found in the folder `login webpage\niab-logo.png`)
- Main heading of: Harvest Data
- Main navigation menu with the items:
  - Features
  - Pricing
  - Help
  - Contact
- A login box with:
  - Username field
  - Password field
  - Login button
  - Forgot your password hyperlink
