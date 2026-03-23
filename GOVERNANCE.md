# Project Governance

TechKnowMad Labs operates its open source projects under a clear, transparent governance model that balances rapid innovation with community input.

## Decision-Making Authority

### Technical Authority

**The CTO holds final authority on all technical decisions** within TechKnowMad Labs open source projects. This includes:
- Architecture and design decisions
- Technology choices and dependencies
- Code quality standards and enforcement
- Performance and scalability requirements
- Breaking changes and deprecations
- Release scheduling and versioning

The CTO commits to:
- Explaining technical decisions transparently
- Considering community feedback before finalizing decisions
- Escalating conflicts to the CEO when necessary
- Documenting rationale for major architectural choices

### Community Participation

While the CTO holds final authority, the community plays a critical role:
- All technical discussions are open on GitHub
- Pull requests receive thorough review and feedback
- Feature requests are discussed with community input
- Concerns are addressed before implementation
- Breaking changes include deprecation periods and migration guides

## Community Contributions

### Pull Request Process

1. **Submission**: Fork the repository, create a feature branch, and submit a pull request
2. **Review Timeline**: All PRs receive initial review within 5 business days
3. **Feedback**: Reviewers provide constructive feedback and request changes as needed
4. **Iteration**: Contributors update their PR based on feedback
5. **Approval**: PR is approved once it meets code standards and aligns with project goals
6. **Merge**: Only maintainers (TechKnowMad team members) merge PRs to main branches

### PR Review Standards

- Code follows the project's style guide (black, mypy, pytest)
- Tests are included for new functionality (90% coverage target)
- Documentation is updated where applicable
- Commit messages follow L0-L7 layer convention
- No security vulnerabilities or code smells
- Performance impact is considered for critical paths

### Contributing Without Code

Contributions beyond code are valued equally:
- Documentation improvements
- Bug reports with reproduction steps
- Feature suggestions with use case examples
- Security vulnerability reports
- Translations and localization
- Community support and mentoring

## Release Cadence

### Scheduled Releases

- **Monthly Releases**: Core projects (Edgecraft, PEP, ITERAI) release on the first Monday of each month
- **Security Releases**: Released immediately for critical security vulnerabilities
- **Patch Releases**: Hotfixes for critical bugs may be released between scheduled releases
- **LTS Releases**: Designated releases receive long-term support (12-24 months)

### Release Versioning

All public projects follow Semantic Versioning (semver):
- **MAJOR**: Breaking changes or significant new features
- **MINOR**: Backward-compatible new features
- **PATCH**: Bug fixes and minor improvements

Example: `2.1.3` (Major.Minor.Patch)

### Release Preparation

- Release branch created 2 weeks before scheduled release date
- Feature freeze: No new features after release branch creation
- Bug fixes only on release branch
- Release notes prepared with contributor attribution
- Changelog updated with all changes since last release

## Feature Requests

### Submitting a Feature Request

1. **Search Existing Issues**: Check if the feature has been requested before
2. **Open an Issue**: Use the "Feature Request" template with:
   - Clear description of the proposed feature
   - Problem it solves or use case
   - Potential alternatives considered
   - Examples or mockups (if applicable)
3. **Community Discussion**: Engage with feedback from maintainers and community
4. **Implementation**: Once approved, may be implemented by you or the team

### Feature Triage

Features are triaged by priority:

| Priority | Examples | Timeline |
|----------|----------|----------|
| Critical | Security, data loss, widespread breakage | Next release |
| High | Commonly requested, significant improvement | 1-3 releases |
| Medium | Nice-to-have, moderate benefit | Backlog |
| Low | Edge cases, niche use cases | Icebox |

## Breaking Changes

### Deprecation Process

Breaking changes follow a strict 3-month deprecation period:

1. **Announcement**: Breaking change is announced in release notes (MAJOR.minor.patch)
2. **Deprecation Warning**: Code produces warnings for 3 months (approx. 3 releases)
3. **Documentation**: Migration guide provided in docs
4. **Communication**: Highlighted in all release notes during deprecation period
5. **Removal**: Breaking change is enforced in next MAJOR version release

### Example Timeline

| Release | Action |
|---------|--------|
| v3.0.0 | Deprecation announced, warnings added |
| v3.1.0 | Deprecation period continues |
| v3.2.0 | Deprecation period continues (final month) |
| v4.0.0 | Breaking change enforced, old behavior removed |

## Roles and Responsibilities

### Maintainer

**TechKnowMad Labs team members**

Responsibilities:
- Review and approve pull requests
- Merge approved changes to main branch
- Manage releases and versioning
- Maintain project documentation
- Moderate community discussions
- Triage issues and assign priorities
- Make final technical decisions (under CTO authority)

### Contributor

**Anyone with at least one merged pull request**

Responsibilities:
- Follow Code of Conduct
- Contribute high-quality code and documentation
- Participate in code review (reviewing others' PRs)
- Help with issue triage and bug verification
- Mentor newer contributors

Privileges:
- Can be assigned to issues
- May be invited to private discussions
- Recognized in contributor list

### Advisor

**Invited domain experts and community leaders**

Selection:
- Nominated by CTO or existing Advisors
- Must demonstrate deep expertise in relevant domain
- Track record of positive community contribution

Responsibilities:
- Provide strategic guidance on major decisions
- Review architectural proposals
- Help mentor contributors
- Participate in quarterly roadmap planning

Privileges:
- Early access to roadmap and planning
- Direct communication with maintainers
- Input on breaking changes and major features

## Governance Meetings

### Quarterly Planning

- **When**: First Monday of each quarter (Jan, Apr, Jul, Oct)
- **Attendees**: Maintainers, Advisors, select community leaders
- **Agenda**:
  - Roadmap review and planning
  - Priority setting for next quarter
  - Resource allocation
  - Community feedback synthesis

### Monthly Retrospectives

- **When**: Last Friday of each month
- **Attendees**: Maintainers and interested community members
- **Agenda**:
  - Release review and metrics
  - Community feedback and trends
  - Process improvements
  - Upcoming challenges and solutions

## Escalation Path

### Issue Resolution

1. **Discussion**: Issues are discussed in the GitHub issue thread
2. **Decision**: Maintainers make decisions based on community input
3. **Escalation**: If consensus cannot be reached, CTO makes final decision
4. **Documentation**: Decision and rationale are documented in the issue

### Conduct Violations

See CODE_OF_CONDUCT.md for enforcement guidelines.

## Amendments to Governance

This governance document may be amended by decision of the CTO. Significant changes will be announced in project announcements and discussed with the community before implementation. The minimum notice period for non-emergency changes is 30 days.

## Contact

- **Governance Questions**: admin@techknowmad.ai
- **Technical Decisions**: CTO via GitHub discussions
- **Community Conduct**: conduct@techknowmad.ai
