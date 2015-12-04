afp-talk
--------

A presentation about The AFP Project.

Abstract
--------

The *Amazon Federation Proxy* (AFP) is a set of tools to easily bridge office,
private- and public-cloud.

When using *Amazon Web Services* in an enterprise environment, the problem of
authenticating staff at scale with the *Identity and Access Management* (IAM)
arises. Of course, one can simply setup an account for every member manually
and require everyone to generate and store static credentials on their local
development machines in the office. This problem is known as *human
authentication*. Secondly, many existing companies have existing compute
resources in a data-center or private cloud. The question arises again how to
allow existing resources to communicate with the AWS cloud.  Again one solution
is to generate accounts for each resource in the data-center and store
static-credentials on those machines. This problem is known as *machine
authentication*.

However, permeating the environment with static-credentials is a bad-idea in
general. They are easy to loose, easy to commit accidentally to github and hard
to rotate systematically. Luckily, AWS provides a mechanism to circumvent this
issue by using the *Secure Token Service* to supply temporary short-term
credentials that simply need to be refreshed on a regular basis. Of course a
solution for integrating this with the company *Active Directory* (AD) and/or
*Lightweight Directory Access Protocol* needs to be established. This is known
as a *Custom Federation Broker*.

In this talk I will introduce the various components of The AFP Project,
developed at Immobilienscout24 GmbH,  which allow us to conveniently make use
of temporary credentials for both human and machine authentication.

:afp-core:  The core federation broker that interfaces AD with IAM.
:afp-web:   A web interface to forward users with appropriate credentials to the
            Amazon Management Console.
:afp-cli:   A command-line interface to the afp-core that allows developers to
            obtain temporary credentials for local use on machines in the
            office.
:afp-proxy: A system daemon that replicates the *Instance Metadata
            Service* (IMS) available on EC2 instances and supplies machines in
            our datacenter/private-cloud with temporary credentials.
