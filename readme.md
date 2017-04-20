# Fair Districts PA Website

## Fair Districts PA Web Development Process

Hello! Thanks for joining this project and offering your time and skills as we build and maintain the FDPA website. The purpose of this document is to outline principles and processes for development, so that we can build quickly while also creating a site that is maintainable in the future by anyone who has time to help.

This document is also going to be helpful for everyone as we review code and add features; my hope is by documenting what we're aiming for as clearly as possible, everyone is able to join in the process of shaping the site's codebase.

### Working Constraints

**1. This site will be relevant for 2+ years**

The legislative process for passing Redistricting reform is a long process and this site will be the canonical source of all web content for FDPA during that period. Our timeline for development is short but the maintenance period is long.

**2. We Don't Know Who Will do Maintenance**

As FDPA is all volunteer led, we should work with the assumption that new volunteers will be helping out occasionally. We should be empathetic towards their learning curves and try to ease them now by avoiding [technical debt](https://en.wikipedia.org/wiki/Technical_debt).

### Principles

**1. Prioritize Simple over Clever**

Everyone who has worked on any web project knows that you can always be refactoring to do things more cleverly or without so many lines of code. Since we don't know who all will be working on this site or their level of experience, we should try to make our code as easy to follow as possible and prioritize clear naming and structure.

**2. Prioritize Equality**

FDPA is trying to make our government more fair to every citizen, this website should reflect that goal. We'll be testing regularly to ensure accessibility guidelines are covered. If you want to brush up on what this means, awesome! Here's [18F's accessibility overview](https://pages.18f.gov/accessibility/) or check out [Vox Media's](http://accessibility.voxmedia.com).

**3. Prioritize Documentation**

Whenever possible, code should have comments with relevant contextual information. CSS should include notes about how to use it if it's a helper class, HTML should include comments about where the markup is output and what it's pulling from, etc. As much as possible I'd love for anyone to open any file in the site and be able to have some context for the impact of any changes they will make and where they should look to find related information.

----

## How to Work on the Site Locally

(WIP Document)

The FDPA site is built on Craft CMS. Craft is fairly easy to work within but it requires you spin up a few things on your computer. This page has everything we know so far about how to do that. If you run into any issues, please document your fixes here.

### Setting up Environment File

This setup comes with [nystudio107](https://github.com/nystudio107)’s Craft multi-environment config. This is preferable to storing and editing the setups in the `config.php` and `general.php` files.

The setup is simple:

**1. Duplicate and rename `example.env.php`**

As the step says, you need to duplicate the `example.env.php` file and rename it to `.env.php`.

**2. Add your server data to `.env.php`**

The variables are detailed in the file, but are presented here, as well:

- `CRAFT_ENVIRONMENT`: The Craft environment we're running in ('local', 'staging', 'live', etc.).
- `DB_HOST`: The database server name or IP address. Usually this is 'localhost' or '127.0.0.1'.
- `DB_NAME`: The name of the database to select.
- `DB_USER`: The database username to connect with.
- `DB_PASS`: The database password to connect with.
- `SITE_URL`: The site url to use; it can be hard-coded as well
- `BASE_URL`: The base url environmentVariable to use for Assets; it can be hard-coded as well
- `BASE_PATH`: The base path environmentVariable for Assets; it can be hard-coded as well 

### Getting Setup

**1. Install MAMP**

[Download MAMP here](https://www.mamp.info/en/downloads/) and install it if you don't already have it. It will also install MAMP Pro in your applications folder; just delete that folder, you won't need it.

**2. Install Sequel Pro**

If you don't already have it, [download and install Sequel Pro](https://sequelpro.com/download).

**3. Open MAMP and start Servers**

You may have to walk through some installation first, but once MAMP opens up, click the Start Servers button. Once Apache and MySql are showing as started, click Open Webstart Page.

**4. Get your Local MySQL Config Info**

On the start page, there's a section labeled MySQL. The values in that section are what you can use to login to your local MySQL instance with Sequel Pro. Type in the values listed on the MAMP page in the corresponding fields in Sequel Pro and login.

**5. Create Database named fdpa**

Once you're logged into Sequel Pro, you can create a database called `fdpa`, all lowercase is important.

**6. Visit the site and make sure it shows up**

Visit `localhost:8888` in your browser. You should see a `begin` button. Click it, walk through the setup process, which allows you to create your user.

**7. Import the existing db**

In Sequel Pro, [TODO: how to import db]

----

## Useful Craft Links

- https://craftcms.com/docs
- https://craftcms.stackexchange.com/
