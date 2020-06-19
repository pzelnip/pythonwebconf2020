# Secure the Snakes! Tips for Secure Development in Python

<https://twitter.com/hayleydenb>

Developers are asked to solve complex problems and balance competing
interests--and sometimes security may fall by the wayside. It is easy enough to
consider security as "somebody else's problem", but that attitude can come back
to bite us. This talk will cover secure coding practices (for both general
Python development and Django development) that you can incorporate into your
work. Every step towards more secure code is a win!

---

## Understanding Vulnerabilities in your open source dependencies

snyk.io to generate dependency tree

Dependencies are the majority of your surface attack area, and they are far more likely to have _known_ security vulnerabilities

Automate tracking vulnerabilities in Python with pyup.io, pyenv, and snyk.io

---

## Are people who they say they are?

Don't roll your own auth
Don't store plain text passwords
use 2FA on personal accounts & try to offer on your project if possible
Django doesn't throttle user auth by default, you should use a complementary tool to do so (ex: Django Defender)

<https://github.com/jazzband/django-defender>

---

## What Should I Know About Permissions?

Be as granular as practical
It is always easier to grant additional perms than try to revoke one
Think about your permimiters

---

## Should I trust this mysterious package?

Trust but verify? NO
Verify and then trust
Assume anything that comes to you from outside could be compromising

### Injection

Write raw SQL sparingly, if at all

Also string formatting should be done carefully in general

### User Uploads and Deserialization

Is your user uploading a picture? Check that it is and not (say) a script. Not being careful with upoads can expose you to risks of code execution

## Protect your Source Code

Follow good hygiene regardless of whther the repo is private or public.
Don't commit sensitive info
You could always have a problem from within your own house and you should act accordingly

## User Data

Be selective (do you need to collect or store that?)
You can't lose data you never collected
View personal data like glitter - if it's out it's really hard to get back & you have no control over where it goes

---

Link to my slides: <https://docs.google.com/presentation/d/1wopCK0nYej7ECaz0hPOHeuCsMKmZHOYDeiPUQ05GHdM/edit?usp=sharing>
Python security: <https://res.cloudinary.com/snyk/image/upload/v1551550455/Python_Security_Best_Practices_Cheat_Sheet__rev.pdf>
Django Security: <https://snyk.io/wp-content/uploads/django_security_cheat_sheet.pdf>
