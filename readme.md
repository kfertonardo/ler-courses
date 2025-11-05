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

To do this, we'll keep an entry for each courseNumber for each unique Title. The combination of a courseNumber and title will allow us to identify the correct course in a given AY

It will also be helpful to add a startAy for the first time a given course was offered and, for those course numbers that have been recycled, and "endAy" marking the last academic year that this course with this course nubmer was taught.


For example: 

```
 {
    "courseNumber": "PL*401",
    "uniqueId": "",
    "title": "Peace and Justice Studies Caps",
    "tags": [
      "Seminar"
    ],
    "note": "",
    "startAy": 25
  },
  {
    "courseNumber": "PL*401",
    "uniqueId": "",
    "title": "Morals&Politics Lord of Rings",
    "tags": [
      "Seminar"
    ],
    "note": "",
    "startAy": 7,
    "endAy": 18
  },
  {
    "courseNumber": "PL*403",
    "uniqueId": "",
    "title": "Philosophy of Happiness",
    "tags": [
      "Seminar"
    ],
    "note": "",
    "startAy": 12
  },
```

TODO: It is hope that during the switch to WorkDay, each course will be assigned a unique id that will also be avaialble to section course listings. If so, the expirationAY will become obsolute and we can begin to use the property "uniqueId" to accurately pinpoint course descriptions.
