# Pharmadex reference data

Read-only distribution location for versioned, signed Pharmadex medicine reference bundles.

**Status: publication pending redistribution review. No public catalogue is available yet.**

The intended stable endpoint is:
https://github.com/RunicSaf/Pharmadex-Data/releases/latest/download/manifest.json

Approved releases will contain reference.zip, a signed manifest, coverage and catalogue reports, checksums, source attribution and source-state metadata. The manifest names an immutable release asset in this repository. The Android application verifies signatures and checksums before installation.

## Source and licensing review

Sources are NHS dm+d (via licensed TRUD access) and the public NHSBSA English Prescribing Dataset with SNOMED codes. No NHS endorsement is implied.

- https://www.nhsbsa.nhs.uk/pharmacies-gp-practices-and-appliance-contractors/nhs-dictionary-medicines-and-devices-dmd
- https://opendata.nhsbsa.net/dataset/english-prescribing-dataset-epd-with-snomed-code
- https://isd.digital.nhs.uk/trud/users/guest/filters/101/licence/1
- https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/

This repository does not itself grant redistribution permission. Before publishing processed NHS assets, the owner must record the accepted TRUD item-24/GTIN licence, downstream account-free redistribution rights, third-party conditions and attribution requirements. Public publication is disabled until that review is recorded and approved in the private builder.

Never upload raw TRUD XML/archives, credentials, private signing keys, patient records or user photographs.

## Maintainer setup

Use a fine-grained publishing token restricted to this repository with Contents read/write. Configure the private builder's protected nhs-data-publication environment and required reviewers. Set DATA_REPOSITORY=RunicSaf/Pharmadex-Data, DATA_PUBLISH_TOKEN, and only after approval DATA_PUBLICATION_APPROVED=true and DATA_LICENCE_REVIEW_URL.

An existing validated candidate can be promoted by the private builder without regenerating NHSBSA months. The original signing identity is retained. Published versions are immutable; a draft becomes latest only after validation. Keep the application source repository private.
