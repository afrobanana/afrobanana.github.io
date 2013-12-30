# The website of The ABR

The purpose of the website is to inform and engage visitors on anything ABR-related.

---

**Current Version**: *chingan*

---

The website contains the following sections:

* Home
* Blog - A place to post anything new related to related to ABR and/or its members.
* Events - A place to post information and media about upcoming events related to ABR and/or its members.
* Sounds - A place to post audio media (new releases, sets, etc) related to ABR and/or its members.

Mini-sites, ie. sites created for a one-off event, are created on their own repo (and subdomain) and are linked to from this website.

This simple structure provides consistent and never-changing URLs for the actual content, and complete flexibility for creating any number of, and for any purpose, mini-sites.

## Examples
The ABR is hosting a new event.

1. A new event post is created
        Using the ``_TEMPLATE`` file in ``_posts/events`` create a new file called ``YYYY-MM-DD-TITLE.markdown``, where ``YYYY-MM-DD`` is the date of the event and ``TITLE`` is a very short version of the title of the event.
2. Add information and media about the event. You can include Flickr galleries, YouTube & Vimeo videos, and SoundCloud, MixCloud, & BandCamp sounds.
3. Save.

### Local Build
```
jekyll build --config _config_local.yml
jekyll serve --watch --config _config_local.yml
```

or just

```
jekyll serve --watch --config _config_local.yml
```

### AWS S3 Sync
```
cd afrobanana.github.io/
aws --profile default --region eu-west-1 s3 cp static s3://afrobanana/chingan/static --recursive --exclude static/css/src/*
```



