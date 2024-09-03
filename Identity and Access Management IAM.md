
-: Hello, and welcome everyone.

So, here in this section,

we are gonna learn about one of the very important module

inside the GCP,

IAM.

Which is nothing but Identity and Access Management.

So what is here, the Identity and Access Management?

So it's a fine, grained access control

and visibility for centrally managing all cloud resource.

So, this particular module product will help us

that to which user we should queue what kind of control

and all those control for every single services

and a product available inside the GCP

one can centrally manage it.

So you know plain English,

it says that,

who can do what

on which resources.

So, let's try to dissect all of three,

who,

what,

and which.

So, who is here like a identity, a member.

In a very layman term, I would say it's email address.

So we have already learned about those

five different identity,

like either it'll be a Cloud Identity domain,

or a Google workspace, Google groups,

or normal Google regular personal account.

Or it can be a service account

but we didn't do much dive into service account.

In upcoming section, we'll have a much more detailed

discussion on service account.

So, who here means a identity.

What that means, our roles.

Roles are nothing but a collection

of different kinds of permission.

So which user,

who can do what,

but on which particular resources.

Now resources can be like Compute Engine,

App Engine, BigQuery, Pub/Sub,

Cloud Proc, Cloud Prep, Kubernetes Engine,

Cloud Function, anything.

So this IAM will help us to define a policies

like who can do what on which resources?

So, if I just try to put everything together,

who, what and which,

it'll be something like some X person

can create VM in Compute Engine.

So, Compute Engine here it's like resources.

Create VM, that means a some kind of role,

that will be, what.

And access nothing but, who. Some kind of identity.

Let's take one more example,

like why can delete and create bucket

inside the cloud storage.

So cloud storage are nothing but are resources,

whereas these are delete and a create bucket

is nothing but a kind of action.

You can say like a collection of permission

that is nothing but our roles.

And why is nothing but some identity.

And this identity can be anything

from those five identity, which we have learned earlier.

All right, so IAM got defined,

we need to focus upon three things.

One is identity, another one is role,

and roles are nothing but a collection of permission.

So lot of permission combined together

will create a role.

Because you just cannot give anyone permission like,

just create bucket permission.

Instead of that there are list of permission

which can be combined to create a roles.

And the third one will be, combine both of them,

which is nothing but a policy binding.

So this particular statement, what we have learned,

X can create a virtual machine inside the Compute Engine.

That means a kind of policy, it is trying to bind identity,

roles and resources.

So, let's try to understand both of them in detail,

identity and roles.

So as far as identity are concerned

we have already learned in earlier section.

So those of you who have not learned about this identity

they can always go back and refer to the section related

to Cloud Identity.

So one of them is our personal account Google account.

We have a non-human account like a service account.

We have a organization based,

two kinds of account, Cloud Identity domain

and a Google workspace.

And when you want to put multiple accounts

in a one single bucket, you can use the Google Group.

So that is the kind of identity.

Now, who this particular identity?

We need to assign some kind of roles.

So let's try to dissect what is roles.

So mainly there are three kinds of role.

One is Primitive.

Then we have a Predefined roles

and we have a Custom role.

Now, in case of Primitive role,

we have a three standard roles are available

like owner, editor,

and viewer role.

So that is like a very broad level access

one is giving at a project level,

although in one of the separate video,

we'll have a detailed discussion on this

primitive kind of roles.

But once you assign such a kind of role

like owner, editor and a viewer,

it won't be applicable on just some resources only.

It'll be applicable at a full project level.

So, all those resources you are gonna provision

inside the project will get such a kind of role.

But then Google has defined a granular control

on your roles.

So roles you can define on some kind of

single services only.

Let's say I want to assign to some person,

compute admin role.

So, it'll be applicable on a

Compute Engine virtual machine only.

Or I want to assign, let's say, network viewer role.

One can see all those network configuration

has been defined under your project

or maybe under your organization.

So I can provide like a network viewer.

Or let's take one more.

Let's say inside the BigQuery,

I want to assign a role for job user.

That means one can just execute BigQuery job inside

the BigQuery environment.

So this roles doesn't apply at whole project level

but at individual resource level.

So that will be definitely a preferred role

but still if your requirement doesn't get satisfied

we have a custom role.

So, these Custom roles are like a customized role,

and can be created from Predefined role.

So, let's say you have some Predefined roles are available

and Google has already created lots of,

hundreds of Predefined role

for different GCP services for us.

Now, from this Predefined role,

you want to remove some permission,

you want to add some permission,

and you can always create a custom role.

So that is about roles.

But what exactly contains inside this owner role

or maybe compute admin role or BigQuery job user role?

Or some kind of Google App Engine related roles.

What is inside this viewer role?

So that is nothing but a permissions.

Roles are nothing but a collection of permission.

So, let's see about structure of this permission.

So, first thing here is on which service you are applying?

Then we have a resource type, then last one will be verb.

Let's see, few examples. So you'll have a much more idea.

Like, Bigtable.tables.cat.

So here Bigtables are something like services.

All kind of products I would say.

Then a resource type.

So inside the Bigtable we have our data sets,

we have tables and many more things.

So on which type of resource you want to

define this permission.

So that will be on a table.

Now, on this table, what is the verb?

What action you want to perform?

Like you want to get the table information,

you want to list the table,

you want to execute something on a table.

So that is how permissions got defined.

Let's see, one more.

Cloudfunctions.functions.list.

So here cloud functions are like services,

functions are resource type,

and list, that means that is like a verb

that what action you want to perform.

Storage.objects.create.

So inside storage services, resource type object,

what you want to do, like delete.

Delete is nothing but a verb.

Or we have a compute.test.create.

So inside the compute engine you can create a desk.

All right, so that is some of the example of permissions.

Now combine this kind of permission,

will create...

If you combine this thing, it will create a role.

And that's how Google has already defined

hundreds of different Predefined role.

Now if as I told, if your requirement doesn't get satisfied,

you can combine permissions from different products,

different services, and you can definitely create

your own custom role.

So it'll be a custom...

Now you just cannot assign such a kind of permission

directly to the user.

You can only assign roles.

And these roles are nothing but a collection of permission.

Even if there is just one permission inside the role,

that's okay.

But directly, a permission users cannot assign to the user.

You have to put this permission in a roles

and this role you can assign to the user.

All right,

so that is the idea about Identity and Access Management.

In the upcoming videos, we'll have a detail discussion

and a complete hands on on different kinds of role.

Like, first we'll take on Primitive role.

And I'll see you in the next video.

Autoscroll

## Course content

## Overview

## Q&AQuestions and answers

## Notes

## Announcements

## Reviews

## Learning tools