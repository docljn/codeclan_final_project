# School Calendar

## The problem
Roughly once a month, the school sends out an email with an attached pdf newsletter.  The final section of the newsletter is "Dates for your Diary" covering a rolling three month period.

Reading the newsletter on a mobile phone is really difficult, as a pdf is not responsive and you have to zoom and scroll all over the place to see what you need.  The newsletter font is also not easily readable: the size is inconsistent and it is cursive.

I often don't remember to add the dates to my personal calendar, and so forget to arrange time off work for special events.

If the dates change, there is no easy way to find the original date and update the calendar reminder, so if I have actually got around to adding things to my calendar I can end up with duplicate entries and make plans around the wrong date.

## Considered solutions
1. A wordpress-compatible calendar which the school website could use.
  - updated automatically when the newsletter is generated
  - with the ability to add the calendar output to my google calendar / iCal / whatever other format exists
  - to be aware of
    - the school already has an internal electronic calendar, and a paper diary, which they use to create the dates list
    - the school does not want to have dates visible more than 3 months ahead, as previously people got very upset when dates changed.

2. A searchable record of school events
  - updated automatically when the newsletter is received OR used to generate the "dates for your diary section" for the newsletter and/or the website calendar from an internal school record
  - a way to select a specific event to add that alone to your calendar in whatever format applies
  - a way to automatically add a calendar notification when you add a school event to your personal calendar

## MVP

### Data Collation
- find a way to get information programmatically from a pdf into a spreadsheet or other easy-access format

### Data Organisation
- convert the data into a consistent format with date: description
- store the data in an easily-accesible structure: csv, db, ??

### Data Presentation
- display events in date order

## Extensions

### Data Cleansing
- look for duplicate descriptions with differing dates (within a specific time frame?) and reconcile
  - potentially ask for user input if not identical...
- ensure that events covering Dec/Jan across years go into the correct year

### Data Presentation
- ensure that only current and future events are displayed
- search option


## Research
### Wordpress Calendars
- constraints:
  - free
  - school website appears to use twenty-twelve wordpress theme
  - single-step update from data file

## Potential Extensions
- individual class blogs have docx downloads of what they are doing this term: would be much better as a blog post!
