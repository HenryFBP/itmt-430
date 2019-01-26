# Two case studies

I chose:
- [A Case Study: WordPress Migration For Shift.Ms](http://highscalability.com/blog/2016/2/3/a-case-study-wordpress-migration-for-shiftms.html)
- [How Uber Manages A Million Writes Per Second Using Mesos And Cassandra Across Multiple Datacenters ](http://highscalability.com/blog/2016/9/28/how-uber-manages-a-million-writes-per-second-using-mesos-and.html)

## A Case Study: WordPress Migration For Shift.Ms

This was a case study that involved a company migrating to WordPress from a
custom webserver.

### What market does that company serve? (What do they do?) And have they always served that market?

[Shift.ms](shift.ms) serves people who suffer from Multiple Schlerosis.

Presumably, they have always served that market since there's not much else
clients a company/platform named that would server.

### What Operating System(s) are used?

It could have been anything, since WordPress runs on many platforms.

Their custom webserver could have also ran on anything.

### Why do you think those were used?

N/A

### What programming languages/frameworks are used?

They used:
- A custom webserver
- WordPress
  - A plugin called BuddyPress for avatars
- A custom database with its own unique schema
- Custom functionality through PHP that interacted with the database.

### Why do you think they were used?

Presumably, this site was custom-built when it was very small and thus more
robust and scalable solutions were never needed.

This case study is just _them needing to upscale_ and they're finally getting
around to it.

### What storage and what database technologies are used?

MySQL and WordPress.

### What is the current stock price and what was the IPO of the company? (if traded publicly.)

Not public.

### What major obstacle (cost, system performance, QPS, etc, etc) was the company trying to overcome by implementing this technology stack?

Likely lack of robustness, lack of scalability, and perhaps new features.

### What can you learn from this article relating to technology architecture?

Mainly that with custom servers (usually) comes custom migration procedures.

If you've got a pile of hand-modified, very custom configuration files, code,
and/or procedures intended to only ever be done by someone 'in-the-know', you'll
have to "pay for that" kind of customization later down the line if you ever
want to migrate.

It is a unique type of "tech debt" that accumulates, similar to poorly-written
code or the lack of documentation.

The more customization outside of the context of a system that can re-generalize
your data, the more extra work there is to generalize that data manually later.

A lot of time was spent analyzing WordPress' database structure, and simply
planning how to:
1. Map the data from a MySQL db to WordPress
2. Fix quirks (nonstandard username characters) that the old site imposed,
3. Reindexing posts, blog articles,
4. Migrating user icons to the custom BuddyPress plugin's folder structure
   (think `uploads/avatar/<ID>/<ID>-thumb.png`, etc) from the old system
5. Migrate features that relied on the old serving them up data in a certain
   way.
   
   Certain functionality such as videos, tips, a "nerve center" (popular posts)
   would need to be recreated within WordPress.

## How Uber Manages A Million Writes Per Second Using Mesos And Cassandra Across Multiple Datacenters

### What market does that company serve? (What do they do?) And have they always served that market?

Uber is a logistics company that facilitates matching drivers with riders.

They let drivers drive riders small (or big) distances and pay them based on
distance, premium features (no co-riders) and other things.

They take an ~25% cut.

They also facilitate delivery from take-out-only places or places that do
deliver, among other things.

### What Operating System(s) are used?

Probably Linux, Solaris, and *nix derivatives.

### Why do you think those were used?

### What programming languages/frameworks are used?

Mesos and Cassandra are the big names.

#### Mesos
Mesos is a way to abstract large amounts of distributed computing power away
into a single "machine".

You can have a manager that spins up and down machines to meet the demands of a
workload.

#### Cassandra

Cassandra is a scalable database.

### Why do you think they were used?

Because they meet the needs (constant uptime and correctness) that Uber
requires. 

They are also not bound to any specific hardware provider, and lets Uber deploy
their own physical machines with Cassandra and Mesos on them.

### What storage and what database technologies are used?

MySQL and Schemaless.

### What is the current stock price and what was the IPO of the company? (if traded publicly.)

It's prrrrrivate! (for now)

### What major obstacle (cost, system performance, QPS, etc, etc) was the company trying to overcome by implementing this technology stack?

They previously had statically partitioned machines, and each machine was customized for a specific service.

This made unified control of services hard.

Each service was one per machine, with no overlap. So, lots of potential wasted.

### What can you learn from this article relating to technology architecture?

A lot about good technologies to use if you want a VERY scalable app.

It also tells you quick details about what each (FREE!) platform does and why
it's useful to Uber.
