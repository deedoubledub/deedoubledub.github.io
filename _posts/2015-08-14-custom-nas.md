---
layout: post
title: 'Custom NAS'
date: 2015-08-14
categories: technology
---

Wow, it has almost been another year. I'm not very good at this. I have
migrated the website once again. This time I am using ghost. I have opted to
ditch the fully custom website because writing any content felt too much
like work. Jekyll is still awesome and I am using it for some sites at my
day job.

My home server infrastructure, on the other hand, is one thing that I am
still doing fully custom. Here is the post I promised nearly a year ago of
the rackmount NAS server that I built last summer.

# Goals For This Build

- Get a NAS - I had a small NAS appliance that had died about year earlier that I wanted to replace.
- It must be rack mounted - Oh yeah, I have a server rack in my house now.
- It must be low power - This is in my house and electricity isn't free.
- It must be quiet - This is in my house and in my current configuration, the rack is sitting next to my regular computer workstation.

Additionally, it did not need to be huge. I am not storing massive amounts
of data. This server's primary duty is media storage and backup for my
desktop. Later it will also provide the storage backend for my VM
infrastructure. The final configuration was 4TB (3.5TB actually
available).

# The Shopping List

[Supermicro A1SAM-2550F](http://www.supermicro.com/products/motherboard/Atom/X10/A1SAM-2550F.cfm)

This motherboard packs quite a bit of power in a small package. It includes
the Intel Atom C2550 SoC, a decent quad-core processor that requires very
little power and outputs very little heat. The processor is passively
cooled, making this board perfect for a low power and low noise server.

[Supermicro SuperChassis 113MTQ-330CB](http://www.supermicro.com/products/chassis/1U/113/SC113MTQ-330C.cfm)

I selected this case because it works well with my chosen board and further
supports the low power goal. It can house more disks than my motherboard
can handle, but using 2.5" drives uses less power than using 3.5" drives.

[Crucial 16GB DDR3 ECC UDIMM x 2](http://www.amazon.com/gp/product/B008EMA5VU)

I bought 32GB of ECC RAM because this server is going to run FreeNAS and ZFS
loves its RAM and it loves the data to be accurate.

[WD Red 1TB 2.5" Drive x 6"](http://www.amazon.com/gp/product/B00EHBES1U)

I needed 2.5" drives to fit my case and because they use less power. WD Red
drives are designed for NAS duty and 1TB was either the largest capacity
available in this form-factor or the largest capacity that fit my budget.

[Kingston 8GB DataTraveler USB Drive x 2](http://www.amazon.com/gp/product/B004TS1J18)

This server is going to run FreeNAS where the OS is typically installed on a
USB drive and isolated from the data drives. The motherboard also has a nice
USB port soldered directly onto the board, which is perfect for this setup.
I bought two, so I have a backup available.

# The Build

# One Year Later

I built this server 13 months ago and it has been running FreeNAS with a
RAIDZ2 volume like a champ every since. The only issue that I have ever
eencountered was an error on the OS drive when FreeNAS started using ZFS on
the boot partition. It turns out that cheap USB drives tend to be faulty. It
was simple to replace the drive and get the system running again without any
data loss.
