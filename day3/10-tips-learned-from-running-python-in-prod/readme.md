# 10 Tips Learned from Running A Python [Pyramid] Web App in Production

<https://github.com/mikeckennedy>

Are you new to running web apps in production? Do you have that nagging feeling
that you should improve the ways you structure, deploy, and develop your app?
Want to see some lessons learned from running a group of Pyramid web apps on a
cluster of Linux servers? Join the talk as Michael Kennedy, founder of Talk
Python, as he shares his top 10 list of lessons learned running a variety of web
apps over the past 5 years. This talk is open to all frameworks. Whether you use
Pyramid, Flask, or Django, most of the tips and tricks will apply to your web
apps you're building and deploying today.

---

<https://github.com/mikeckennedy/python-virtual-conf-web-tips>

---

Tip 1 - Use Secure.py

<https://secure.readthedocs.io/en/latest/>

---

Tip 2 - static content served through nginx

also gzip it

cache_id as a query param

---

Tip 3 - Let's Encrypt

---

Tip 4 - Design Patterns

ViewModel example, separation of concerns
Services
Structured folders

---

Tip 5 - Error logging and reporting

logbook <http://logbook.readthedocs.io/>
Sentry

---

Tip 6 - Not Storing Secrets

<https://direnv.net/>

---

Tip 7 - 80/20 testing with sites

Use sitemap.xml to request all non-auth endpoints.

---

Tip 8 - Site speed

Google Pagespeed insights for guiding efforts

---

Tip 9 - Activate a venv at server login

Only applicable for when you manage the server

---

Tip 10 - Dependencies

Pyup and dependabot
