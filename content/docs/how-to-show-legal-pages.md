+++
title = "How to show Legal Pages"
description = "Display your own Privacy Policy and Terms of Service"
weight = 0
draft = false
toc = true
bref = "Follow this quick tutorial to know how to add your own Privacy Policy and Terms of Service"
+++

Starting from Fider 0.13, it is now possible host custom Privacy Policy and Terms of Service that will be displayed to all users during the registration and sign in process.

<h3>Prerequisites</h3>

You will need both documents written in a markdown format, they **need** to be named `terms.md` and `privacy.md`.

<h3>How to</h3>

Fider's Docker image expects both file to be available on `/app/etc`. You can copy these files anywhere you want on your server and share them with your Docker container by using [volumes](https://docs.docker.com/storage/volumes/).

E.g.: if both files are on `/home/me/fider`, you can map it to the container with `-v /home/me/fider:/app/etc`.