http://nvie.com/posts/a-successful-git-branching-model/#why-git

##Main Branches

###Master
We consider origin/master to be the main branch where the source code of HEAD always reflects a production-ready state.

###Develop
We consider origin/develop to be the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release. Some would call this the “integration branch”. This is where any automatic nightly builds are built from.  When the source code in the develop branch reaches a stable point and is ready to be released, all of the changes should be merged back into master somehow and then tagged with a release number.

##Supporting Branches

Unlike the main branches, these branches always have a limited life time, since they will be removed eventually.

###Feature branches
- May branch off from: develop
- Must merge back into: develop
- Branch Naming Convention: anything except master, develop, release-*, or hotfix-*

Used to develop new features for the upcoming or a distant future release.  The essence of a feature branch is that it exists as long as the feature is in development, but will eventually be merged back into develop or discarded.  Feature branches typically exist in developer repos only, not in origin.

###Release branches
- May branch off from: develop
- Must merge back into: develop and master
- Branch naming convention: release-*

The key moment to branch off a new release branch from develop is when develop (almost) reflects the desired state of the new release. At least all features that are targeted for the release-to-be-built must be merged in to develop at this point in time. All features targeted at future releases may not—they must wait until after the release branch is branched off.

When the state of the release branch is ready to become a real release, some actions need to be carried out. First, the release branch is merged into master.  Next, that commit on master must be tagged for easy future reference to this historical version. Finally, the changes made on the release branch need to be merged back into develop, so that future releases also contain these bug fixes.

###Hotfix branches
- May branch off from:master
- Must merge back into: develop and master
- Branch naming convention: hotfix-*

They arise from the necessity to act immediately upon an undesired state of a live production version. When a critical bug in a production version must be resolved immediately, a hotfix branch may be branched off from the corresponding tag on the master branch that marks the production version.

When finished, the bugfix needs to be merged back into master, but also needs to be merged back into develop, in order to safeguard that the bugfix is included in the next release as well.
