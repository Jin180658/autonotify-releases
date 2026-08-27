# AutoNotify Releases

This repository contains public AutoNotify installer releases and the update
manifest used by installed copies to detect a newer version.

It intentionally contains no application source code, customer data, database
backup, `.env` file, or credentials.

For each release, publish the installer as a GitHub Release asset and update
`latest.json` to point to that exact HTTPS asset URL.
