# Steady Bytes Hugo Theme

A Hugo theme used by Steady Bytes. Modified from the original [Apsho theme](https://github.com/StaticMania/hugo-apsho) by Static Mania.

## Getting Started

Create a directory and optionally a git repository for your new website:

```shell
mkdir website
cd website
git init
```

Add the theme as a git submodule:

```shell
git submodule add https://github.com/steady-bytes/theme.git themes/steady-bytes
```

Copy the example site from the theme:

```shell
cp -r themes/steady-bytes/example/* .
```

Run the site in development mode and access the site at the provided link in the logs:

```shell
hugo server
```

## Using the theme

Customizing the theme is simple. Below you'll find all the ways to adjust this theme to suit your needs.

### Colors

Open the file `assets/scss/_variables.scss` and you'll see all the colors built into the theme that can be customized. Play around with these and you'll see the site live update in your browser.

### Settings

Open the file `hugo.toml` and you'll see a bunch of options to configure. You can adjust a lot of things here like the navigation bar, the logo, contact info and more!

### Sections

The main page is broken up into a bunch of different sections. Each of these has a corresponding `.yml` configuration file under the `data/` directory. Open each one up and change text, image links, and even enable/disable options like buttons and lists!

### Subscriptions

Subscriptions for this theme are designed to be handled by [listmonk](https://listmonk.app/) which is a free and open-source newsletter and mailing list manager. Follow their documentation for setting up your own server. After you do, to enable email subscriptions simply open the `data/subscribe.yml` file and edit both the `submitURL` and `listUUID` to match your server and desired email list.

**NOTE**: Make sure to also add your website's privacy policy to the `content/privacy.md` file before accepting subscriptions!

### Adding pages

Adding a new page to your site is pretty simple. Create a file with the path `content/<YOUR_PAGE_NAME>/_index.md` and open it. Within the file add the contents (you can always change this later):

```txt
---
title: <YOUR_PAGE_NAME>
---
```

After this, we need to add the HTML to render it. Look through the `themes/steady-bytes/layouts/` directory to select a template that is similar to what you need or just create your own from scratch. Place that file in the `layouts/<YOUR_PAGE_NAME>/` directory.

Now navigate to your new page!
