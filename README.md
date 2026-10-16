# Credits

Jekyll rakefile: https://github.com/avillafiorita/jekyll-rakefile

## Resume

The resume source of truth is `resumes/resume.json` in this repo. The `hjhart/resume`
repo is archived; this repo is now the source of truth.

### Writing style

Each job has a prose `summary` for context and optional `highlights` (rendered as
bullets) for measurable wins. Keep them consistent:

- **Past tense**, even for the current job. Start each sentence with a verb: "Scaled",
  "Built", "Led", "Reduced". Drop the subject; use "I" only in the prose summary where
  it already reads naturally.
- **Lead with what you did, then the result.** Include a number whenever one exists
  (patients, revenue, percent, minutes, headcount). Say "from X to Y" for growth.
- **Plain words.** Say "built" not "leveraged", "ran" not "spearheaded". No buzzwords,
  no marketing tone.
- **One idea per bullet**, one or two sentences, ending in a period. Don't repeat the
  same metric across bullets.
- **Name the tech only when it matters** (e.g. "sharded PostgreSQL"), not as a list.
- **Keep it shareable.** Check that revenue, margin and customer figures are okay to
  publish before adding them.
- Aim for 2-4 highlights per job, most recent job first, strongest bullet first.

Raw data behind quoted figures (commit rates, etc.) lives in `resumes/data/`.

### Generate HTML

```
cd resume && docker-compose build && docker-compose run --rm resume ./node_modules/.bin/resume export --theme short resume.html
```

The generated `resumes/resume.html` can then be saved as PDF from Firefox (File → Save as PDF).

### Upload

```
scp resumes/resume.* deploy@hjhart.com:/home/www/hjhart_com/_site/resumes/
```

## Run server

```
docker-compose up
```

## How to deploy

```
docker-compose run --rm app bundle exec cap production deploy:upload_site
```

## Static build

```
docker-compose run --rm app jekyll build
```

## Create a new post

```
docker-compose run --rm app bundle exec rake create_post['title goes here']
```
