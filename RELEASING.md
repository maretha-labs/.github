# Releasing a project to maretha-labs

The checklist every public release in this org passes. Every release, every time.

## Scope

Projects here are original Maretha work unless their README names another source. For a
collaboration fork of a third-party project, preserve the public source attribution and
applicable license. Do not replace third-party licenses with MIT or claim company-only
authorship. Record the canonical upstream and the reviewed source commit. Scan the inherited
history and the proposed default-branch tree before release. Keep fork workflows manual and
disable inherited publishing jobs that target another organization's infrastructure.

## Checklist

1. **Tracked files only:** build the release from `git archive HEAD` - gitignored and untracked
   files never travel.
2. **Placeholder pass.** Replace everywhere, including comments and docs:
   - cloud account IDs, zone IDs, distribution and pool IDs
   - bucket names, hostnames, IPs, repo slugs (owner/repo) outside this org
   - team usernames and email addresses outside one intentional contact point
   - project identifiers that are not part of the public story
   Deliberate brand stays: the company name, logo, and the showcase domain in prose.
3. **Make required what cannot ship a default** (domains, bucket names, repo slugs). A
   reference repo must fail loudly, not deploy someone else's values.
4. **Add or refresh:** LICENSE (MIT), SECURITY.md (private contact), and README security notes
   that disclose every known trade-off. Shipping a trade-off silently is the only wrong option.
5. **Disable push-triggered CI** (workflow_dispatch only) so day one is not a failed run.
6. **Verify the code still works post-edit:** language syntax checks, `terraform validate`, or
   the project's equivalent.
7. **Scan:** gitleaks on the tree AND the history, plus a grep battery of every known
   environment-specific value. Both must come back empty.
8. **Wording:** no README, notice, changelog, commit message or repo description calls a project
   a mirror, snapshot, export or rewrite of other code, or names another repository as its
   source. Third-party sources are named explicitly.
9. **History:** a single commit per branch, company authorship only.
10. **Publish:** push to maretha-labs, set the repo description and topics, and add the project
    to the org profile README.
