# Project planning

## Challenges

- unreliable power
- computer scarcity (but proliferated cellphone ownership)
- datacenters not in Africa
  - latency
  - flaky network router peering
- latency could cause update problems
- minimal standup, maintenance cost

## Questions

- Browser stats of teachers?
- How best to ensure reliable accounting?
  - unique database feature(s)
  - batching and queuing
  - [ACID](https://en.wikipedia.org/wiki/ACID) vs [BASE](https://en.wikipedia.org/wiki/Eventual_consistency)
- School composition [MCSS Schools](https://mcssliberia.org/schools/)
  - Are there school districts?
- Do teachers:
  - Share classrooms?
  - Specialize(do kids change classrooms for different classes?) or generalize(teach same students all day)?
  - Teach multiple groups if children ? (A day, B day)
- Is attendance for just classes or should it include exams?

## Architectural attributes

- open source
- robust stack

### front end

- mobile first
- cache-able front-end (pwa)
- efficient data exchange w/API
  - RESTful
  - GraphQL
- Separate admin/analyst interface

### Back-end

- lightweight API call-based
- time series data

## Technologies (ideation)

### Front end framework options

- [Astro](https://astro.build/)
- [Preact](https://preactjs.com/)
- [Vue](https://vuejs.org/)
- [Mithril](https://mithril.js.org/)
- [SolidJS](https://www.solidjs.com/)
- [Svelte](https://svelte.dev/)
- [Lit](https://lit.dev/docs/)
- Written off for size reasons
  - React
  - Angular
  - Ember

### Backend options

- [Flask](https://flask.palletsprojects.com/en/2.2.x/#)
- [Django](https://www.djangoproject.com/)
- [FastAPI](https://fastapi.tiangolo.com/)

### Database options

#### General relational databases

- MySQL
- PostgreSQL
- MariaDB

#### Time series databases

- [InfluxDB](https://www.influxdata.com/influxdb-pricing/)
- [TimescaleDB](https://www.timescale.com/) (built on top of PostgreSQL)
- [AWS Timestream](https://aws.amazon.com/timestream/)
- [OpenTSDB](http://opentsdb.net/)

## Working definitions

- School: A building or group of buildings considered a single institutional entity
- Classroom: single room at a school where groups of students and teachers participate in class sessions (poorly worded)
- Teacher: Person who teaches and takes attendance
- Student: Person who attends classes and receives lessons
- Subject: A lesson plan that us used to teach a class
- Class: A schedule of lessons covering a subject given by a specific teacher to a prescribed group of students
- Lesson: A single scheduled session of a class

## Data model

 *not started- dependent on answers to open questions above*

- Schools
- Classrooms
- Teachers
- Students
- Subjects
- Classes
- Lessons

## References

- [Monrovia Consolidated School System (MCSS)](https://mcssliberia.org/)
- [SIS-MCSS GitHub repo](https://github.com/code4nova/SIS-MCSS)
- [How to Make PWAs Installable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Installable_PWAs)
- [Learn PWA](https://web.dev/learn/pwa/)
- [PWA Minimus: A minimal PWA checklist](https://mobiforge.com/design-development/pwa-minimus-a-minimal-pwa-checklist)
