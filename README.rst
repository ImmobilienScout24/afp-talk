========
afp-talk
========


The AFP Project: secure cloud authentication for machines and humans.

Abstract
========

When using *Amazon Web Services* (AWS) services from the outside AWS, there are two main
authentication problems:

* Authenticating humans (employees, users, contributors etc...)
* Authenticating machines (servers, applications, clusters etc...)

At scale, the common practice to use *IDentity and Access Management* (IAM)
users with static credentials / access keys is generally considered
harmful---they are easy to loose control over and hard to rotate systematically
[1]. Hacked credentials are a sought after commodity and allow a digital
adversary to perform anything from mining digital currencies [2] to cracking
passwords.

The *AWS Federation Proxy* (AFP) Project [3], developed at ImmobilienScout24,
solves the issue for both machines and humans by using a *Custom Federation
Broker* and the *Secure Token Service* (STS) with IAM roles and temporary
credentials. This talk introduces the project, the various components it
consists of, and explains how we can use it to largely eliminate IAM users and
static credentials.

* [1]: https://99designs.com/tech-blog/blog/2015/10/26/aws-vault/
* [2]: http://www.devfactor.net/2014/12/30/2375-amazon-mistake/
* [3]: http://immobilienscout24.github.io/afp/

License
=======

Content
-------

All Content is...

* Copyright 2015 Immobilien Scout GmbH
* Licensed under the terms of [Attribution-ShareAlike 3.0 Unported
  `(CC BY-SA 3.0) <http://creativecommons.org/licenses/by-sa/3.0/>`_

Included Dependencies
---------------------

The following dependencies are shipped with the sources:

* Wiki2beamer (file: ``wiki2beamer``) is licensed under Gnu Public Licence v2
* Minted (file: ``minted.sty``) is licensed under LaTeX Project Public License  version 1.3
* ccBeamer (directory: ``creative_commons/``) is licensed under Creative Commons Attribution-ShareAlike 3.0
