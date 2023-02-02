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
title: Digital Hydrant
level: 1
---

# Digital Hydrant

The Network Suck Tool

```
The Groundhog Day Release: v0.9.0
```

<br />

<img src="/groundhog.jpg">

---

# Architecture

<img src="/architecture.svg" class="h-90">

---

# Hydrant

A Hydrant is a device on the target network that serve two functions

<v-clicks>

- It scans the Network
- It Acts as a Honey Pot

</v-clicks>

---

# Collectors

Network Scanner

<v-clicks>

- Netdiscover Local

  ```bash
  arp-scan --local --interval=100
  ```

- Netdiscover

  ```bash
  # We also scan a list of known subnets for misconfigured devices.
  # For example
  arp-scan 10.10.0.0/24 --interval=100
  ```

</v-clicks>

---

# Collectors...

<v-clicks>

- Nmap

  ```bash
  # Once we collected a list of hosts, we scan each host for open ports

  # get open TCP ports
  nmap -sT 192.168.1.1

  # get open UDP ports
  nmap -sU 192.168.1.1
  ```


- Hydra

  ```bash
  # Then we try too log in on these hosts with a list of known usernames/passwords
  hydra -t 4 -I -L users.txt -P passwords.txt -s 22 192.168.1.1 ssh
  ```

</v-clicks>

---

# Open Canary

Honey Pot

<v-clicks>

- FTP
- HTTP

</v-clicks>

---
layout: full
---
# Aggregators

Aggregators are background workers, that extract useful information from the raw measurement data

<v-clicks>

- Hydrant Last Seen
- Canary Alerts
- Device details
- Errors

</v-clicks>

---

# Aggregators...

<img src="/aggregators.svg" class="h-90">

---
layout: image-right
image: /slack.svg
---

# Notifications

<div>We currently support Slack notifications, with plans to support more systems in future</div>
<br />
<v-click>
<img src="/canary-alert.png">
</v-click>

---

# To Do

<v-clicks>

- Organize Hydrants into Users/Orgs
- Improved User Interface
- Wifi scanning
- Remote shell access
- Scale!
</v-clicks>

---

# Demo

<v-clicks>

- Show UI
- Show/Trigger Canary

</v-clicks>
---

# Questions

---
layout: end
---
