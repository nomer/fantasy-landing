# Fantasy Copilot landing page

Public, static landing page for Fantasy Copilot and its privacy policy and terms. The site contains HTML and CSS only—no JavaScript, analytics, or cookies.

Primary URL: <https://fantasy.nomerr.com>

Mirror: <https://fantasy.nomercode.com>

## Keep the mirror in sync

Add the mirror once, keeping its domain-specific `CNAME` commit on a separate local branch:

```sh
git remote add mirror git@github.com:nomer/fantasy-landing-mirror.git
git fetch mirror
git switch -c mirror-sync --track mirror/main
```

After updates are pushed from `main` to `origin`, merge and push the same changes to the mirror:

```sh
git switch mirror-sync
git merge main
git push mirror mirror-sync:main
git switch main
```

The two branches should differ only in the custom-domain `CNAME` file.
