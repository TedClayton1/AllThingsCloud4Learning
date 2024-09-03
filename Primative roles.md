
-: Hello and welcome everyone.

So in this video we are gonna see about the primitive roles.

So primitive roles are like too much broad access

you are giving to the user.

And definitely that is not recommended,

but GCP has already defined in a earlier

when they launch this products.

So in those days,

they were giving such a kind of broad access

at a project level.

It will not be a fine granular access

to individual resources.

So if you just assign some kind of primitive role

as it is applicable on a whole project level,

every single resource can be accessed.

So there is no resource specific role.

And that's why it is not recommended.

It just doesn't follow the principle

of list privileges also.

So what is here the principle of list privileges?

Let's say when new journey join to your organization

under your team, and let's say you want him to do some work

on, let's say, cloud storage only.

And if you just provide a very broad level access

like editor,

definitely he can do anything on a cloud storage.

That's perfectly fine.

So far so good.

But at the same time there are other hundreds

of different GCP services are available.

And user ideally should not get access on it.

But due to the nature of such a kind of role editor,

one can get a complete access on other resources

which is a part of those project.

So that doesn't follow the principle of list privileges.

You are giving more and more privileges,

and such a kind of user can even harm to your system also.

They can unnecessary create some other kind of resources

which is not at all required.

So in case of primitive,

we have three kinds of roles are available.

One is owner, we have a editor, and we have a reader role.

So in case of reader, we have read-only permission

for all resources inside the project.

So once you assign a reader role,

the user can see all the resources inside project.

But in case of editor, you have all access like a reader,

plus you can do modification in your resources,

you can change the configuration

of any kind of resources you have created,

any kind of state also you can change it.

And then we have a very high-level

super admin kind of role like owner.

So here you will get all access like a editor.

Apart from that, you can even manage user groups

and you can manage a billing part also.

So you can see more and more access you are getting

when you go from reader to editor to the owner.

So definitely here you'll be able to see

lesser number of permission,

and from reader to editor to owner,

you will get more and more number more permission.

So what we will do, let's just go to our Cloud console,

and currently I am inside this GCP PSE project.

Let's go to, from navigation menu, IAM,

and just crawl down, and we have roles.

So let's just try to explore owner, reader and editor.

Now, here Google has given us all those role,

which is predefined and primitive you role.

So if you just scroll it down,

you will be able to see we have a total,

as of recording this particular video,

813 roles are available.

Among them the three roles are primitive role,

owner, editor and reader.

In case of custom role, you can create from here.

see upcoming videos, we'll see about that.

Now in this video, let's just try to understand three roles.

So first, let's filter about the reader.

So either I can code down and keep searching for reader,

or there is a nice filters are available

and you can do the filtration

based on the different property.

So here we can do filtration

based on the different properties

like title we are used in, status.

So what we'll do, you can have a look at individual role

belongs to some kind of services.

But here we are dealing with all those role,

which is at a project level,

not at some specific resource level.

So what I'm gonna do, I'm gonna use this, use them,

and let's just check for project.

Yeah, we have a projects.

And you can have a look at,

we have four roles are available at a project level now:

like a viewer, owner, editor, and browser.

So what we will do, let me open this viewer into another tab

and let's open browser also.

So you can have a look at, this is the roles/viewer.

And there are total 1,963 assigned permission.

Now if you just observe this viewer role,

there will be all those gets

and a list kind of services mostly,

because you are getting access to read

to get to list something.

So for all those services

and a products available inside the GCP,

you will get read-only kind of access.

Now let's just go to browser.

So in case of browser,

we have just a few permissions are available.

And those permissions

are not at some specific resource level,

but it'll be at a folder organization and a projects.

So related to folders, projects and organization,

one can just gag those project, gag those folder.

and list those folders and a project.

So that's a very limited scope.

So one cannot do anything related to any kind of resources.

So that is about the read access to all your resources.

And here they have given in a description

like access to browse GCB resources.

Now, let me go to our first tab.

And I'm gonna open this editor role in another tab.

And we are going to compare this editor

with our viewer role.

So compared to viewer,

we have a 1,963 permissions are available.

In case of editor,

we have 4,089 permissions are available.

And this roles are completely managed by Google,

so you do not need to worry about it.

When some new features will be added,

some new products will be added,

this assigned permission will be automatically updated.

But this kind of role generally nowadays, not preferred one.

Now, when you go from editor to owner, let me open owner.

And let's see how many permissions are available

inside owner role.

So now compared to editor,

we have almost around 300 permission.

More permission has been available inside this owner role.

So it says that full access to all your resources.

So this owner role are something like

editor related all permission

plus some more extra permission

like managing users and groups and a billing information.

All right.

So we have seen about all those primitive role

and we did filter based on the projects,

but we can always do filtration

based on some other titles also.

So let me select this one.

To do the filtration, we how to use such a kind of ID.

So let's say,

I'll just select this one.

And let me remove this folder.

So let me search for viewer.

That will be nothing but roles/viewer.

And you can have a look at our viewer role.

Same way we can search for other roles like editor.

And we have a same way like a owner role.

Now you can see that there is one symbol

with every single role.

So this symbols from GCP,

which indicates that all this role will be managed by GCP.

You do not need to worry about anything.

So there are, as we have seen earlier,

813 predefined roles are available.

Among them, we have seen the four one,

which is nothing but a primitive role.

So that is all about the primitive role.

How to assign this primitive role to individual user

or a predefined role to individual user,

in upcoming videos, we'll see about that.

Now, next one will be to learn about those predefined role.

Now this is also predefined, but like a very broad access.

But when we learn about the predefined role

with a narrow access to some particular resources

or services, it will be a great fun.

So with this, I'm just ending this video,

and I'll see you in the next video.