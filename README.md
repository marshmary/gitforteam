# Git for Team training project

## Requirements:

> The purpose is setting up a new git repository for a team to development an application.

Team members:

- Development team: 3+ developers, 1 scrum master
- Operation team: 2 operators
- Management team: 1 project manager

Delivery plan:

- 1 Feature Package/2 weeks
- 1 Patch Package/4 weeks
- 1 Production Package/3 months

## Repository set up:

### Access control

**Strategy: Shared maintenance** 

Why? An application will be developed by a team managed by a PM, this means they have a process to help them work together. Shared maintenace approach helps the development faster.

### Branching pattern

**Pattern: Scheduled release**

Why? The project has delivery plan to release new packages. So there is also no required for multi-stage environment application.

![branching pattern](imgs\branching-pattern.png)

### How to

1. Develop new feature

- Create a new feature branch

    Create a new branch from the main branch (e.g. "master") specifically for the new feature you want to release. This branch should be named in a descriptive and consistent manner, such as "feature/feature-name".

- Develop the feature 
    
    Switch to the feature branch and start developing the new feature. Make sure to commit frequently and write clear and descriptive commit messages. Test your feature thoroughly to ensure that it works as expected.

- Use pull requests

    When a team member has finished working on a feature or bug fix, they should create a pull request to merge their changes into the main branch. This allows other team members to review the changes before they are merged, which helps catch errors and ensure that the code meets the team's standards.

2. Review code

- Review and merge code
    
    When a pull request is created, team members should review the changes and provide feedback. Once the changes have been reviewed and approved, they can be merged into the main branch.

- Resolve conflicts

    Sometimes, team members may make changes to the same file or code at the same time, resulting in conflicts when trying to merge the changes. When this happens, the conflicts must be resolved before the changes can be merged. Make sure everyone on the team knows how to resolve conflicts using Git.

3. Release a new package

- Create a release branch:

    Create a new branch from the main branch (e.g. "master") specifically for the release. This branch should be named in a descriptive and consistent manner, such as "release/release-version-number". The version number should correspond to the version of the software release.

- Make final changes:
    
    Make any final changes to the software that are necessary for the release, such as fixing bugs, updating documentation, or removing debugging code. Commit these changes to the release branch.

- Test the release:
    
    Test the release thoroughly to ensure that it works as expected and doesn't introduce any new bugs or issues.

- Merge the release branch into the main branch:
    
    Once the release is complete and tested, merge the release branch into the main branch (e.g. "master"). Before merging, it's important to make sure that the main branch is up-to-date with any changes made by other team members. Resolve any conflicts that arise during the merge.

- Tag the main branch:

    Create a Git tag for the commit that corresponds to the new software release. The tag should be named using the software version number to make it easy to identify. For example, if the new version is 1.2.0, the tag should be named "v1.2.0".

- Push changes to the remote repository:

    After merging the release branch into the main branch and tagging the main branch, push the changes to the remote repository. This will make the new software release available to other team members and users.

- Update documentation and release notes:

    Update any relevant documentation, such as user manuals or API documentation, to reflect the new software release. Write release notes to inform users and stakeholders of the changes and improvements included in the new release.

