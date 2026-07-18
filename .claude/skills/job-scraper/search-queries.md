# Search Queries for Job Scraper

<!-- Candidate is open to fully remote roles only, not tied to Denmark. The built-in
     jobindex.dk / jobbank / jobdanmark / jobnet CLI tools in this framework are
     Denmark-specific and are not used for this search. Queries below rely on
     LinkedIn and Google site-searches against remote-first job boards instead. -->

## Search Sites

Primary (remote-first job boards):
- **linkedin.com/jobs** - filter by "Remote"
- **weworkremotely.com** - remote-only listings
- **remoteok.com** - remote-only listings, strong on dev roles
- **himalayas.app** - remote-only listings
- **wellfound.com** (formerly AngelList Talent) - startup roles, many remote
- **arc.dev** - remote developer-focused board

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Every query should be combined with "remote" (the candidate does not filter by city/region - full-remote only, no relocation).

### Priority 1: React Native / Mobile Developer

These match the candidate's strongest and most desired career direction.

```
site:linkedin.com/jobs "React Native Developer" remote
site:linkedin.com/jobs "Mobile Developer" React Native remote
site:weworkremotely.com "React Native"
site:remoteok.com "react native"
```

### Priority 2: Senior / Lead Mobile Engineer

Growth-direction roles - candidate wants to move toward senior/lead mobile engineering.

```
site:linkedin.com/jobs "Senior React Native Developer" remote
site:linkedin.com/jobs "Senior Mobile Engineer" remote
site:linkedin.com/jobs "Lead Mobile Developer" remote
site:wellfound.com "Senior React Native"
```

### Priority 3: Frontend / React Developer (adjacent)

Adjacent roles the candidate could pivot into, given strong React.js and TypeScript experience.

```
site:linkedin.com/jobs "Senior Frontend Developer" React TypeScript remote
site:linkedin.com/jobs "React Developer" remote
site:remoteok.com "frontend" react typescript
```

### Priority 4: Broader / Full-Stack (wider net)

Candidate is learning Node.js toward a future full-stack pivot - not a current requirement, but worth an occasional wider-net search as skills develop.

```
site:linkedin.com/jobs "Full Stack Developer" React Node remote
site:linkedin.com/jobs "JavaScript Developer" remote
site:himalayas.app "React Native" OR "mobile developer"
```

## Location Filter

The candidate is open to **fully remote roles only** - no commute range, no relocation.

- **Ideal**: Fully remote, any timezone, async-friendly
- **Acceptable**: Fully remote with reasonable timezone overlap (e.g. within ~4-5 hours of West Africa Time / UK time)
- **Borderline**: Remote-first but requires occasional travel to an office (flag for user discussion)
- **Too far / exclude**: On-site required, hybrid required, or relocation required - these are hard deal-breakers

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries

If the user later wants to add other portals (e.g. region-specific remote job boards), extend this file - see `/add-portal`.
