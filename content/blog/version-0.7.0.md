+++
date = "2017-10-31"
title = "Fider 0.7 released with members administration and automatic SSL"
categories = ["releases"]
description = "We're happy to announce that Fider 0.7 is now available"
author = "goenning"
+++

### 1. Add/Remove Members

This <a href="https://feedback.fider.io/ideas/24/allow-other-users-to-be-adminstrators">feature has been suggested</a> during the month and received a few votes on a short amount of time. 
This is a really basic feature that we were missing and now we're happy to ship the first version of it on this release.

<figure>
  <img src="/images/blog/add-remove-members.gif" />
</figure>

### 2. Technical Improvements

This release was all about Technical Improvements. We've <a href="https://github.com/getfider/fider/pull/136">removed echo</a>, <a href="https://github.com/getfider/fider/pull/140">updated React to v16</a>, <a href="https://github.com/getfider/fider/pull/148">increased code coverage</a>, <a href="https://github.com/getfider/fider/pull/144">removed other dependencies</a> and refactored a lot of code.

All these changes allowed us to have better runtime and compile performance, smaller repository size and a better code organization.

### 3. Experimental feature: AutoSSL powered by Let's Encrypt

I've been researching about automatic SSL with Let's Encrypt for a while and finally decided to give it a try on Fider. On this release, we're including a new environment variable called <code>SSL_AUTO</code>. When this is enabled, Fider will use <a href="https://godoc.org/golang.org/x/crypto/acme/autocert">autocert</a> to automatically fetch a free SSL certificate for your application.

Al you have to do is add <code>SSL_AUTO=true</code> to your environment variables. Please note that, because of Let's Encrypt requirements, your application must be publicly available with a valid domain name.

Make use of this great feature and share your thoughts/issues with us through <a href="mailto:admin@fider.io">admin@fider.io</a>.

### How to update

Running an old Fider version? Don't worry, the upgrade process is just a matter of updating your Docker container to the latest stable image on Docker Hub. Use <code>getfider/fider:stable</code> to make sure you're always running the stable version.

### What's next?

It's up to you!

Visit our [feedback forum](https://feedback.fider.io/) and raise your voice. Tell us what to do next!