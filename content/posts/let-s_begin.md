---
title: "Let's begin 2"
date: 2019-11-05T23:48:08+01:00
draft: false
toc: false
images:
tags:
  - Github
  - actions
  - AWS
  - s3
  - cloudfront
  - hugo
---

This is the start of my personal blog.

I will somewhat continuously deliver some thought on what is going on around me in the world of tech and programing.

## How is the site built

This site was setup in AWS, using [terraform](https://www.terraform.io/) (a declerative language/tool for provisioning resources) for its infrastructure, and [Hugo](https://gohugo.io/) (GoLang based static site generator).

I love terraform for all of its simplticty. I use use it professinally and personally for all of the cloud resources that I provision. I have tried both AWS CloudFormation, and Azures Resource Manager, but I find my self always returning to terraform.

Hugo was just a choice of tools that I heard used by a colleague, and I found it easy to use.
Secondly, since I knew that you could serve a static site through AWS S3 with AWS CloudFront in front of it, it sounded perfect.

My second kind of hope for this project, was to explore how GitHubs featuire `Actions` worked. It's basically the same as a GitLab Runner; a pipeline that runs on events and checked in code.
So, this site is currently being written in Markdown and each time I check changes in to GitHub; my pipeline verifies the code, builds it, and publishes it to AWS S3. When the CloudFront distribution notices that theres a change in an object, it fetches the new content and serves it to the world.

## What did I learn

### Certificates

At first, I had a domain that was registered with an external (to AWS) domain registrant.
Connecting them, i.e. point the domain to the name servers of my hosted zones name servers in AWS; proved to be more dependant on the external domain registrant than I thought. The issues came once I tried issuing a certificate for my domain, and when registring ownership of the domain.
So, eventually I switched over and registered a new domain within AWS, and the connection went flawless.
