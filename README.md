# Skans.jl

[![CI Test][ci-img]][ci-url]
[![Website][site-img]][site-url]

[ci-img]: https://github.com/rikhuijzer/Skans.jl/workflows/CI/badge.svg
[ci-url]: https://github.com/rikhuijzer/Skans.jl/actions?query=workflow%3ACI+branch%3Amain

[site-img]: https://img.shields.io/badge/Skans-website-blue.svg
[site-url]: https://poweranalyses.org

Monitor web pages and get notified when a page has changed.

## Features

- Scan a list of web pages for changes
- For each page, specify which region of the page has to be checked
- Run the checks on a schedule (specified via a CRON job; powered by GitHub Actions)
- Get notified when a page has changed

## Use-cases

Monitor pages for:

- New job offers
- Availability (error detection)
- Updated product pricing
- New (financial) reports or other news
- Updates to legislation

## Example

To check <http://example.com> and <https://bbc.com> for changes, create a new GitHub repository and copy the contents of

[.github/workflows/Skan.yml](https://github.com/rikhuijzer/Skans.jl/blob/main/.github/workflows/Skan.yml)

into your own repository.

After doing this, Skans will check the web pages for changes and add an issue comment in your repository every time a page changed.
The downloaded pages are stored in the `skan` branch of your repository to be able to compare them on the next run.

