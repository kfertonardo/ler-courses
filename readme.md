# A Machine Actionable Course Catalogue

The most important task is to add task by which slices of courses can grouped and compared. 

# Reserved Tags

* "exclude"
  * add the exclude tag to any unique or one-off course that should be included from fill rate analysis
* "1stLevel"
  * reserved for classes that are considered a first level core course
* "2ndLevel"
  * reserved for classes that are considered a second level core course
* "Lab"
* "Seminar"
  * A catch all tag for major level courses. If that is not sufficiently refined, then new tags should be introduced.
* "Ethics"
* "Graduate"
  * reserved to designate a course as a graduate course. By default all courses are considered "Undergraduate". In other words, the "Undergraduate" tag will be applied to all courses that are NOT tagged "Graduate"

# Course numbers, unique ids and expiration dates

With unique ids in our catalogue or section reports, and since course numbers eventually get recycled, we will need a way to uniquely identify courses. 

For this we will use an expiration date. 

For a course number that has been removed and perhaps even re-used, we will add a property called "expirationAY": which should indicate the last AY in which this number was used for this course (the AY number is always defined by the spring year of a given AY, e.g. 23/FA is AY 24).

We will use this expiration year to currently identify a section from a given year and its course metadata. If three courses return for section 201 in AY 24, then consider whether AY comes before or after the expertionAY and thus discover which course description applies.

TODO: It is hope that during the switch to Workday, each course will be assigned a unique id that will also be avaialble to section course listings. If so, the expirationAY will become obsolute and we can begin to use the property "uniqueId" to accurately pinpoint course descriptions.

For example: 

```
 {
    "courseNumber": "PL*401",
    "uniqueId": "",
    "title": "Morals&Politics Lord of Rings",
    "tags": ["Seminar"],
    "note": "",
    "expirationAY": 18
  },
  {
    "courseNumber": "PL*401",
    "uniqueId": "",
    "title": "Peace and Justice Studies Caps",
    "tags": ["exclude"],
    "note": ""
  },
  {
    "courseNumber": "PL*403",
    "uniqueId": "",
    "title": "Philosophy of Happiness",
    "tags": ["Seminar", "social-political"],
    "note": "",
    "expirationAY": 12
  },
```
