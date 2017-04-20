Technical standards for Developing on the Site:

## Browsers

We're going to test on and support all evergreen browsers (Chrome, Firefox, Edge, mobile), last two versions of Safari, IE11 and newer.

## PR Process

Master is a protected branch in Github. That means you can only add code to it via a Pull Request. Make sure all changes you make are on a branch and then use that branch for opening the PR.

Along with this, please preface your branch with `feature/` or `hotfix/`. Most work will be a `feature/` branch, so if you're styling the events page you might `git checkout -b feature/event-page-styling`, which will create the branch and let you start working.

Once you are ready for your code to be reviewed, push it to github and open the PR. Ping #github-prs in slack and let people know it exists. Once someone else has reviewed/signed off on it and you think it's ready to go, merge it in.

## Deploying

TBD
