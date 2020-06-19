# Nornir: Solve Big Problems Fast

<https://github.com/lykinsbd>

Managing over 60,000 network devices can be a mind-boggling and difficult task.

Over the years at Rackspace, we have tried many tools and frameworks to help us
wrangle this problem, with varying degrees of success.

Recently, we’ve begun making use of Nornir to rapidly solve some of our complex
and pressing issues.

Nornir, as a native Python automation framework, allows us to leverage our
existing Python based infrastructure, applications, and libraries and generate
meaningful and powerful APIs and services for our end users and administrators.

By utilizing Nornir’s built in Inventory, Task, and Result handling framework,
we can quickly solve a problem and have an application from prototype to
production in under a week.

This allows our network developers to focus on solving the problem at hand, not
on reinventing the wheel for every new API or application that is needed

---

Python automation framework

"What about ansible?"

Nornir Ain't Ansible

no DSL
Logic in Code, not YAML
100% Python

---

Anything you can access via ssh you can use Nornir to automate

Easily integrated with other Python frameworks

Fast: <https://networklore.com/ansible-nornir-speed>

---

## Nornir Concepts

- Inventory
  - hosts
  - groups
  - defaults
- Tasks
  - actions on hosts
  - essentially python functions but with free goodies/magic

---

Overview of Nornir Basics, how to get inventory, configure & run tasks, etc

---

## Use Cases

Example of company X buying company Y & using Nornir to plug into Comp Y's existing Flask app.
