# Fireside Chat w/Carl Meyer from Instagram

Interactive Q & A with dude from Instagram

Some questions:

---

What are some of the differences going from a small startup doign a Django
project to the largest scale Django project in the world Instagram?

Talked about things like long-lived feature branches no longer being an option
at all. Need to break everything into tiny pieces that can be continually
integrated with mainline.

---

Switch from Python 2 to Python 3, thoughts?

Use static typing, watch for unicode strings being an issue, etc.

Use of unit tests being run in Python 2 & Python 3 in CI.

---

What version of Python 3 are you running?

P3 was initially 3.5, now at 3.7, discussions ongoing.

---

Microservices vs Monolith

Continuous deployment of entire codebase every 10 minutes

Dependency/version problems go away in monolith archs.

Pros/cons both ways.

Have extracted some things into services. Ex: contained problem spaces, needs to
be rewritten in other languages, etc.

Largely have embraced the monolith.

---

Things we should (or should not) adopt in Python from other languages?

should: static/gradual typing!

should not: skipped, too controversial. :p

---

Scaling: async vs sync, benchmarks & fallacies

Over last year or two, have moved server codebase to entirely async.

Async is a tool, evaluate as such (what problem do you have, will this tool
help?)

Specific probleM: monolith is large, therefore memory heavy, worker processes
would take up a ton of memory thereby preventing more fully utilizing CPUs,
async solves that

For small sites, probably not be an issue.

Async fn calls are 1.5x slower than synchronous in Python, so that overhead can
be prohibitive.

---

How do you do code review in such a large project that's always being deployed?

Everything has to be reviewed, somebody else in the company can review it, and
once approved process is automatic after that.

use fabricator.

Single branch model!

After merge about 30 mins later it's in prod.

Tons of automated tests, some AI that helps by being selective about what tests
run on the PR, when merged all tests run.

Initial deploy is canary, deployed to 3% of servers, then over time gets
automatically rolled out across the fleet

150 releases per day, release every 10 mins during primetime hours.

CD has complexity too, no branch complexity, but now have problem with how do
you build big features (hint: feature flags, gates, etc). Cruft can accumulate
over time.

---

30 diffs to run Black, done over time as otherwise it'd just be too big

---

What VCS do you use?

use Mercurial (woah). Some Git for some smaller internal projects.

Mercurial was more hackable, at their scale they have to make changes to the VCS
itself

---

How long do the tests take to run?

Might be over 100k tests now. Run distributed over many machines, takes 10-12
mins.

---

if you don't branch what do your CI/CD mechanisms or practices look like? Not
talking about CI/CD tooling would like to know about the dev culture and
adoption

CI/CD was already well established when he got there. So already baked into the
culture at the org.

---

How do you train new devs in this manner (ie on CI/CD)

At their scale, there's no option. If they came in with a different mindset
they'd "pretty quickly learn their lesson" because so much changes in the
codebase with so many people all working on it.

---

How do you handle backward incompatibility changes (ex: db migrations)

A lot of things become "more work", but there's no way around it. Can't do
synchronized db migrations. Assume forward/backward compatibility, and break
into series of safe small changes.

---

How does instagram deal with images on the backend? are image adjustments
handled entirely on the client apps or does insta use Pillow or other image libs

Much manipulation is done on the client.

Not entirely sure on specifics.

Points to how since the product is so massive, no one person knows it all.

---

Are you enforcing Black as a code checker?

Yup, part of CI.

---

Has that been an advantage?

Devs have loved it, consistency is awesome. Obs you can find edge cases where
the formatting is weird, but those are fare outweighted by consisteny and not
having to argue about formats.

---

How do you perf test or load test before stuff gets into prod?

tool that can spin up specific version of the code and replay real prod traffic
against it & give metrics on cpu usages, etc

monitoring in prod of canary deployments.

small regressions do get out from time to time, toolchain to detect those, auto
file a task for the dev who introduced the fault

---

What would you encourage new devs to level up on, improve their career, etc?

A) build things a lot
B) as you do, be curious about the tools you're using and how they work
