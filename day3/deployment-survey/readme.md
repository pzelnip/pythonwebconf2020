# A Brief Survey of the Web Deployment Landscape

Beginning a new project or entering a new environment, it can be daunting to
sort through the options and requirements of various deployment strategies. This
talk aims to provide you with a baseline familiarity with a few popular patterns
that can aid you in determining what will work well for your application and
your organization. We'll discuss:

- distinguishing characteristics of various deployment methods
- the core value of deployment as a step in the software lifecycle
- the costs, benefits, and implementation of certain practices
- factors that might influence/restrict your choices

---

Joined late

## Build Practices

- static analysis
- dependency resolution
- vulnerability checking
- execute unit tests
- manual code review
- semantic versioning
- packaging (eggs, wheels, docker containers, golden VM images)
- distribution: upload the release/artifact to a package service or artifact
  store

## Ship Step

Can execute from:

- a CI server
- repository service
- config mgmt esrvice
- infra provider
- locally

Can include:

- env creation
- infra preparations
- config injection
- launch of a release/artifact
- new instance health checks
- directing traffic to the release/artifact
  - detailed discussion of canary, blue/green, A/B testing, feature flags, etc
- rollback to previous release/artifact

Tuned out partway through.
