---
# try also 'default' to start simple
theme: default
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Digital Hydrant Slide Deck
# persist drawings in exports and build
drawings:
  persist: false
css: unocss
layout: image-right
image: /hydrant.jpg
---

# Digital Hydrant

Tagline

---

# Architecture

<img src="/architecture.svg" class="h-90">

---

# Hydrant


<div v-click>
A Hydrant is a device on the target network that serve two functions:
</div>

<ul>
<li v-click>Actively scanning the Network</li>
<li v-click>Acting as a Honey Pot</li>
</ul>

---
layout: two-cols
---

# Collectors

Network Scanning

<ul>
<li v-click>Netdiscover</li>
<li v-click>Nmap</li>
<li v-click>Hydra</li>
</ul>
::right::

# Open Canary

Honey Pot

<ul>
<li v-click>Ftp</li>
<li v-click>HTTP</li>
<li v-click>...</li>
</ul>
---

# Aggregators

<div v-click>
Aggregators are background jobs, that extract useful information from the raw measurement data
</div>

<ul>
<li v-click>Hydrant Last Seen</li>
<li v-click>Canary Trigger Alerts</li>
<li v-click>List of Devices on a Networ</li>
<li v-click>Errors</li>
</ul>
---
layout: image-right
image: /slack.png
---

# Notifications

---

# To Do
<ul>
<li v-click>Organize Hydrants into Users/Orgs</li>
<li v-click>Wifi scanning</li>
<li v-click>Remote shell access</li>
</ul>

---

# Demo

- Show UI
- Show/Trigger Canary

---

# Questions

