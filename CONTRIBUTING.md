# Contributing to CFTRDataTransfer

Contributions can improve the CFTR import scripts, document the transfer workflow,
or make failures easier to reproduce. Start with the [workflow overview](README.md).

## Before you start

Search existing issues and pull requests before beginning. Describe substantial
changes in an issue so their scope and integration requirements are clear. Use
synthetic examples when discussing laboratory workflows or import failures.

This repository contains VBScript integration with Agena Typer and Cerner
Millennium Helix. Read the bootstrap, configuration and shared-library flow in
the README before changing an import script. Changes to field mappings, sample
matching or result handling need an explicit description of the old and new
behavior.

## Report a bug or propose an improvement

Use the repository's issue template when available. Include the affected commit,
relevant software versions, steps to reproduce, expected and observed behavior,
and a minimal synthetic input. Remove identifiers, credentials and internal
connection details from logs and screenshots. Report security concerns privately
as described below.

## Development and validation

1. Start a focused branch from the current `master` branch.
2. Keep script and documentation changes limited to the stated problem. Preserve
   existing interfaces unless the change explicitly documents their impact.
3. For script changes, document the synthetic input, expected imported fields and
   observed result. Cover malformed input and failure handling where relevant.
4. Run integration checks only in an authorized, isolated non-production
   environment with the required vendor software. Record the environment and
   checks that were actually performed. If that environment is unavailable,
   identify the unverified behavior in the pull request.
5. For documentation changes, check links, filenames and consistency with the
   scripts. The [privacy and secret-scanning workflow](.github/workflows/privacy-secrets.yml)
   must also complete successfully when it runs.

The repository does not currently document a standalone automated script test
command. Do not present a documentation check or secret scan as verification of
clinical result processing. A merged contribution does not authorize deployment
to a laboratory or production system.

## Submit a pull request

Open a pull request against `master`. Explain the problem, the resulting behavior,
any issue it addresses, compatibility effects and validation evidence. Include
regression checks for behavior changes where a suitable harness exists; describe
manual checks and any unavailable integration checks accurately. Update affected
workflow documentation in the same change.

Required automated checks must pass. Follow the repository's existing review
rules and resolve feedback; this guide adds no mandatory second-person approval,
DCO sign-off or contributor agreement.

## Security, licensing and conduct

Follow the account's [security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md).
Use GitHub's private vulnerability-reporting option if available. If a private
route is unavailable, request a private contact without publishing sensitive
details. Never include patient records, real sample identifiers, credentials or
restricted vendor material in contributions.

Submit only material you have permission to contribute. Preserve copyright,
attribution and applicable license terms; clarify unclear reuse permissions with
the maintainer before adding third-party material. Communicate respectfully and
follow the [code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md).

## Basis for this guide

The structure follows GitHub's [contribution-guideline guidance](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
and the contribution-process and acceptable-contribution criteria in
[OpenSSF Best Practices](https://www.bestpractices.dev/en/criteria).
