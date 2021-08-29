---
layout: default
title: Home
permalink: /
---
<p style="text-align:center;">
  <img src="https://i.imgur.com/XOxm3Zb.png" alt="drawing" width="150"/>
</p>
<h3 style="text-align:center;">Open source Discord bot for CTF teams</h3>

## Overview

OvisBot is a modular, feature-extensive Discord bot for managing CTF teams through discord. It facilitates collaboration and organisation by providing well defined commands to create/delete/update discord category/channels in order to structure CTF problems and provide more efficient team commmunication. In addition the bot provides basic utility functions to assist the solving process of CTF challenges (encoding schemes, etc.. ). Finally, promotes competitiveness amongst team members by providing a aut-synchronised leaderboard to common cybersecurity training platforms such as [CryptoHack](https://cryptohack.org/) and [Hack The Box](https://www.hackthebox.eu/).

Note that the majority of the features are provided by isolated plugins and thus they can be enabled/disabled on demand.

This is a self-hosted bot, therefore it requires to be hosted on a private server in order to be used. Further instructions to do so are provided below. It also required a running instance of MongoDB on the server but still, the docker-based installation instructions take care of that. 

To get started, head over to the [Installation Guide]({{site.baseurl}}/installation).