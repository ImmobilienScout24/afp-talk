afp-talk
--------

The AFP Project: secure cloud authentication for machines and humans.

Abstract
--------

When using *Amazon Web Services*  (AWS) from the outside, there are two main
authentication problems:

* Authenticating humans (employees, users, contributors etc...)
* Authenticating machines (servers, applications, clustes etc...)

At scale, the common practice to use *IDentity and Access Management* (IAM)
users and generate static credentials is generally considered harmful---they
are easy to loose control over and hard to rotate systematically [1]. Hacked
credentials are a sought after commodity and allow a digital adversary to
perform anything from mining digital currencies [2] to cracking passwords.

The *AWS Federation Proxy* (AFP) Project [3], developed at ImmobilienScout24
solves the issue for both machines and humans by using a *Custom Federation
Broker* and the *Secure Token Service* (STS) with IAM roles and temporary
credentials.

In this talk I will introduce The AFP Project, the various components it
consist of, and explain how we can largely eliminate IAM users and static
credentials.

[1]: https://99designs.com/tech-blog/blog/2015/10/26/aws-vault/
[2]: http://www.devfactor.net/2014/12/30/2375-amazon-mistake/
[3]: http://immobilienscout24.github.io/afp/
