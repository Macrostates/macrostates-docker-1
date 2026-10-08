# Naming and publishing

Image names and tags should make image identity, version, and intended use clear.

## Image names

Image names should be stable and should identify the project, service, or tool
the image runs.

Project-specific specifications should define concrete image names when images
are part of the supported project interface or deployment model.

Avoid image names that depend on a single developer machine, temporary branch,
or local experiment.

## Tags

Use immutable tags for builds that may be deployed, released, audited, or
compared later.

Useful immutable tags may include a release version, Git commit, build number,
or another stable build identifier defined by the project.

Mutable tags such as `latest`, `dev`, or branch names may be used for
convenience, but they should not be the only way to identify an important image.

Production deployment should not depend on an ambiguous mutable tag unless a
project-specific specification explicitly accepts that tradeoff.

## Labels

Images should include useful metadata labels when practical.

Labels may identify source repository, revision, version, license, build time,
or image purpose. Do not put secrets or sensitive environment details in image
labels.

## Publishing

Pushing images to registries should be an explicit project operation.

Registry names, credentials, publishing permissions, and promotion rules belong
in project-specific specifications or deployment documentation.

Do not publish images from local experiments unless the active workflow and
project-specific rules allow it.
