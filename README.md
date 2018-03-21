# texlive
TeX Live with additional packages.

Docker image with TeX Live full and additional `git` and `curl` to work with CircleCI. It can also push the final `pdf` to Bitbucket Downloads section with:

`curl -X POST "https://${BB_AUTH_STRING}@api.bitbucket.org/2.0/repositories/${CIRCLE_PROJECT_USERNAME}/${CIRCLE_PROJECT_REPONAME}/downloads" --form files=@"output.pdf"`

## Additional support for

- CircleCI

## Usage

Run with `docker run -ti --rm --name texlive -v $(pwd):/texlive/work shyd/texlive pdflatex my-awesome-book.tex`.

## References

- <https://confluence.atlassian.com/bitbucket/deploy-build-artifacts-to-bitbucket-downloads-872124574.html>
