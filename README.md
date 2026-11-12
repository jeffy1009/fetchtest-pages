# fetchtest-pages

Public test page for checking whether Gemini and Bixby can fetch and search a GitHub Pages site.

- Contains only neutral text and test markers. No personal data.
- No `noindex` tag on purpose: the search-path test needs the page to be indexable.
- Delete the repo after testing.

## Publish (once github.com is logged in)

    gh repo create fetchtest-pages --public --source . --push
    gh api -X POST repos/<login>/fetchtest-pages/pages -f "source[branch]=main" -f "source[path]=/"

Page URL: https://<login>.github.io/fetchtest-pages/
