# pull-request-counter

A quick &amp; dirty way to compile a list of pull requests per user

## What's it Do?

It uses Github's API to first pull down a list of users who have starred the
`py-study-group/challenges` repository, and then iterates over that list,
asking Github for a list of pull requests exectued.

## Does it Work?

Mostly.  The output is rather ugly at the moment, but I'll fix that in time.

## Any Caveats?

Yeah, the pull-request counter currently maxes out at the number of entries
Github returns from its API, which isn't a problem unless someone has more
than 100 PRs in the designated window.  Currently the user with the most PRs
has *8*, so I'm not going to worry abou this.

## Usage

```bash
$ ./generate
```

This creates a static file, `index.html` that contains a list of the stats
we're looking for.
