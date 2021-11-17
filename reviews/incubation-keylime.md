| :exclamation:  Please update this file|
|---------------------------------------|

**This document was prepared in Q3 2021 and is designed to be ready to be
picked once enough progress has been made in the Keylime project to submit for
incubation.**
Progress is expected by the TOC in these areas:
- Fully mature Rust re-write of [Keylime
agent](https://github.com/keylime/rust-keylime/)
- more integrations (beyond a POC) with Kubernetes or other projects

Elements that will need updating:
- Users in production
- Project health: current state of contributors
- Project health: commits / releases
- Project health: Keylime enhancements

| :exclamation:  Please update this file|
|---------------------------------------|

# Keylime Incubating Stage Review

Keylime is currently a sandbox project, accepted into the CNCF in September 2020.
For discussion of Keylime's alignment with the CNCF, please refer to the
[sandbox proposal](../proposals/sandbox/keylime.md).

In the time since being accepted as a sandbox project, Keylime has kept growing
at a steady pace and seen several real-world deployments, including a very large
one.


## Incubating Stage Criteria

In addition to sandbox requirements, a project must meet the following
criteria to become an incubation-stage project:

### Successful use in production

**Requirement: Document that it is being used successfully in production by at least three independent end users which, in the TOC’s judgment, are of adequate quality and scope**

  * IBM has deployed Keylime in production on over 5000 servers to provide
    hardware-based remote attestation as part of the IBM Cloud. A CNCF [blog
    article](https://www.cncf.io/blog/2021/07/06/ibm-implements-remote-attestation-on-linux-with-a-hardware-root-of-trust-using-keylime/)
    provides more information on this deployment.

  * ** NOT YET IN PRODUCTION; REMOVE THIS WHEN IT IS **
    [Lernstick](https://www.digitale-nachhaltigkeit.unibe.ch/services_and_support/lernstick/index_eng.html),
    an educational operating system for "bring your own" devices that loads from
    USB drives, is using Keylime to guarantee the integrity of the system being
    loaded on student's computers.


  * ** ADD THIRD USER **

You can see more users of Keylime in the [Friends of Keylime
repository](https://github.com/keylime/friends)

### Project health: contributors

**Requirement: Have a healthy number of committers. A committer is defined as someone with the commit bit; i.e., someone who can accept contributions to some or all of the project**

The project is healthy and moves along at a steady pace, without issues.

The comunity is around 20 people (as seen in the chat), active and
welcoming.

The main repository, the Python implementation of Keylime
([keylime/keylime](https://github.com/keylime/keylime)) saw 26 people
contribute over 250 pull requests, contributing to 7 releases, including a major
version. Keylime is now at version 6.2.0 (2021-09-01).

More indicators of the project's good health are the mean time to merge a PR (5
days, 10 hours), the quality of the conversations on the chat and the regular
appearance of newcomers.

The Rust implementation of the Keylime agent, being developed in the
[rust-keylime](https://github.com/keylime/rust-keylime/) repository, has also
seen considerable progress. A first testable version was made available in July
2021, which led to the discovery and fix of several bugs, including
security-related ones, to the project's overall benefit.

The security fixes have been an opportunity to confirm the current security
process is functional. The project nevertheless intends to improve it.

A [formalized governance policy](https://github.com/keylime/.github/blob/master/GOVERNANCE.md)
has been instituted project-wide. It applies by default to all project
repositories (as well as any new ones that will be created).

Maintainers of the project are listed in our
[MAINTAINERS.md](https://github.com/keylime/keylime/blob/master/MAINTAINERS.md)
file. There are currently 9 maintainers from 7 organisations:
* IBM
* MIT
* Netflix
* Red Hat
* Universität Bern
* ZTE

Maintainers are added and removed from the project as per the policies
outlined in the project [GOVERNANCE.md](https://github.com/keylime/keylime/blob/master/GOVERNANCE.md)
file.

### Project health: commits, contributions

**Requirement: Demonstrate a substantial ongoing flow of commits and merged contributions**


#### Project releases

There were seven [releases](https://github.com/keylime/keylime/releases) since the sandbox application.
Some are mentioned below.

* [v6.2.0 is the latest minor release](https://github.com/keylime/keylime/releases),
  shipped on the 1 September 2021. It added:
    * Feature: New API versioning system to allow smoother upgrades and backwards
      compatability guarantees
    * Feature: Validate ima-buf like ima-ng with exclude and allowlist
    * Requirement: require TLS 1.2  
  As well as making improvements to the documentation, the installer, CI/CD and
minor cleanup, refactors and bug fixes.


* [v6.1.1](https://github.com/keylime/keylime/releases), shipped on 21 July 2021. It added:
    * Feature: AllowLists are now a top level object with API support
    * Documentation: document the measured boot PCRs and what is
      using thems
  As well as making improvements to the installer and minor cleanup, refactors and bug fixes.
  
  Notably, this release removed support for TPM 1.2.

* [v6.0.0 is the latest major release](https://github.com/keylime/keylime/releases),
  shipped on 24 February 2021. This release:
    * Fixed CVE-2021-3406
    * Deprecated TPM 1.0 and Deep Quote functionality
    * Fixd an issue that checked persistent handles
  * Over 250 Pull Requests were merged in the
    [keylime/keylime](https://github.com/keylime/keylime/pulls) repository, and
nearly 350 over all the project repositories (cf.
[devstats](https://keylime.devstats.cncf.io/d/24/prs-merged-repository-groups?orgId=1))

**COMPLETEME**
* Roadmap: check with Michael / Project Lead
**/COMPLETME**

* Keylime Enhancements: Keylime has a [formal process](https://github.com/keylime/enhancements)
    for interested parties to submit new features or other significant changes.
    Since Keylime was accepted as a sandbox project, 12 enhancements were proposed:
    * [4_improve_project_layout.md](https://github.com/keylime/enhancements/blob/master/4_improve_project_layout.md)
    * [7_multi-tenancy.md](https://github.com/keylime/enhancements/blob/master/7_multi-tenancy.md)
    * [16_remote_allowlist_retrieval.md](https://github.com/keylime/enhancements/blob/master/16_remote_allowlist_retrieval.md)
    * [22-enhanced-scalability.md](https://github.com/keylime/enhancements/blob/master/22-enhanced-scalability.md)
    * [23_dedicated_keylime_user_account.md](https://github.com/keylime/enhancements/blob/master/23_dedicated_keylime_user_account.md)
    * [18_migrate_ci_to_gh_actions.md](https://github.com/keylime/enhancements/blob/master/18_migrate_ci_to_gh_actions.md)
    * [23-ima-sig-signature-verification.md](https://github.com/keylime/enhancements/blob/master/23-ima-sig-signature-verification.md)
    * [33-automate-pr-assignees.md](https://github.com/keylime/enhancements/blob/master/33-automate-pr-assignees.md)
    * [38-allowlist-management.md](https://github.com/keylime/enhancements/blob/master/38-allowlist-management.md)
    * [40-tpm2-pre-boot-event-log-support.md](https://github.com/keylime/enhancements/blob/master/40-tpm2-pre-boot-event-log-support.md)
    * [45_api_versioning.md](https://github.com/keylime/enhancements/blob/master/45_api_versioning.md)
    * [47_agent_ip_port.md](https://github.com/keylime/enhancements/blob/master/47_agent_ip_port.md)
    * [46_revocation_severity_and_context.md](https://github.com/keylime/enhancements/blob/master/46_revocation_severity_and_context.md)
    * [48_ima_incremental_attestation.md](https://github.com/keylime/enhancements/blob/master/48_ima_incremental_attestation.md)
    * [53_agent_local_revocation.md](https://github.com/keylime/enhancements/blob/master/53_agent_local_revocation.md)

* Contributors: [https://github.com/keylime/keylime/graphs/contributors](https://github.com/keylime/keylime/graphs/contributors)

* Commit activity: [https://github.com/keylime/keylime/graphs/commit-activity](https://github.com/keylime/keylime/graphs/commit-activity)

* CNCF DevStats: [https://keylime.devstats.cncf.io/](https://keylime.devstats.cncf.io/)
    * [Last 30 days of activity on GitHub](https://keylime.devstats.cncf.io/d/8/dashboards?refresh=15m&orgId=1&from=now-30d&to=now-1h)
    * [Community Stats](https://keylime.devstats.cncf.io/d/3/community-stats?orgId=1&var-period=d7&var-repo_name=keylime%2Fkeylime)

### Versioning scheme

**Requirement: A clear versioning scheme**

Keylime adheres to Semantic Versioning, as mentioned in [RELEASE.md](https://github.com/keylime/keylime/blob/master/RELEASE.md).


### Security

**Requirement: Clearly documented security processes explaining how to report security issues to the project, and describing how the project provides updated releases or patches to resolve security vulnerabilities**

Keylime is a security-oriented project, and it is approached as such. The
codebase is developed with security in mind.

The security process is simple, but functional. See
[README](https://github.com/keylime/keylime/#security-vulnerability-management-policy).

Keylime has only had one security advisory so far and the process has proved
functional.

### Specifications require public reference implementation

**Specifications must have at least one public reference implementation**

Not applicable.
