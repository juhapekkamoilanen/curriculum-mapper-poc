# curriculum-mapper-poc

Live demo of poc https://hy-mapper.github.io/ (only frontend)

![screenshot.png](screenshot.png)

More info in deployment repository https://github.com/hy-mapper/hy-mapper.github.io

## Features for application

- Students can "vote" for prequisite topics for a course
  - Students can see list of courses available for voting
  - Students do not have to sign in to vote
- Teachers can manage (crud + sort) topics for courses
  - no sign in, just a special link as auth
- Students can add a topic for a course
- Teachers ans students can see results for a course
- Teachers can accept new topics (created by students)
  - Teachers see student-created topics in a different color in results
- Teachers can reset votes
- Teachers can add new courses

**Extra**

- Votes are connected to target course topics

**Extra 2**

- Optional: Students cannot see results before voting
  - Teachers can see results with a special link?
  - Students get a view-only link after voting
- Optional: Light-weight sign in
  - Registering: press a button -> site generates a long hash username -> users needs to remember only that to sign in
  - Optional: save hash username to localstorage
  - Three levels
    - Students: View and vote
    - Teachers: Edit topics, add courses
    - Admins: Create teacher usernames

**Extra 3**

- Self-assessment mode: Enable teacher get an understanding of students skill level at the beginning of a course

## Developing

To run locally:

- git clone
- cd curriculum-mapper-poc
- npm install
- npm start

## Deployment

Here's a hacky way to deploy to github pages:

- npm run build
- cd build
- git init
- git add -A
- git commit -m "Deploy"
- git remote add gh-pages git@github.com:hy-mapper/hy-mapper.github.io.git
- git push --force gh-pages master
