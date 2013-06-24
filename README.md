# Fisheries of New Zealand (FINZ)

## Why?

<a href="http://trophia.com">Trophia</a> developed the Fisheries of New Zealand (FINZ) website during a project for
the New Zealand Ministry of Fisheries (now the <a href="http://mpi.govt.nz">Ministry for Primary Industries</a>).

Since then, the project has been incorporated into the work programme 
of <a href="http://fonz.tridentsystems.co.nz">Trident Systems</a> and developed further.

This repository simply sets up a HTML redirect from http://finz.trophia.com to http://fonz.tridentsystems.co.nz.

## How? (Because someone, somehere, someday, might just be interested)

We setup an empty Github pages branch to this repo:

```sh

git clone https://github.com/trophia/finz.git
cd finz
git checkout --orphan gh-pages
git rm -rf .
```

Created `index.html` with the HTML redirect in it (and some other silly stuff no one should ever see)
Then pushed up the changes.

```sh
git add index.html
git commit -a -m "First pages commit"
git push origin gh-pages
```

Created a file called `CNAME` with the one line `finz.trophia.com` in it so that
Github pages knows to point that domain at that `index.html` file.

On our zone file, created an A record for finz.trophia.com pointing to 204.232.175.78 (Github pages).

Done!
