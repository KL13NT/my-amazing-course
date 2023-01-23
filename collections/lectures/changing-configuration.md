---
title: Changing Site Configuration And Theme
description: How to change website metadata and the theme used
published: true
---

## Website Metadata

To change metadata about your course such as course name, campus, or code you
can change the corresponding values in the `cac.config.json` file. Change any of
the values and commit the changes to have them immediately reflect in the output
website.

This is a sample explanation. This is simplified.

## Theme

CaC uses an unconventional approach to styling on the web called Classless CSS.
This approach works by defining a stylesheet for HTML elements only. It does not
contain classes, utilities, or other product-related configurations.

I decided to go with this approach because it makes changing the theme as easy
as it could get, assuming course administrators would be the ones interacting
with the configuration file.

There's a [GitHub repository] listing several classless CSS frameworks that are
all compatible with this project.

For example, if I wish to change the theme to the "Water Dark" theme all
I have to do is make the following changes to the configuration file:

```diff
{
	"courseName": "My amazing course",
	"campusName": "Sample Campus",
	"courseDescription": "A sample course about computer science!",
	"campusWebsite": "https://example.com",
	"courseCode": "CS 101",
- 	"theme": "https://cdn.jsdelivr.net/npm/water.css@2/out/light.css"
+ 	"theme": "https://cdn.jsdelivr.net/npm/water.css@2/out/dark.css"
}
```

> Make sure the URL to the css file actually points to the raw text stylesheet
> and not a webpage, and that you can link to it from your website. CDNs work
> great and include unpkg.com and jsdelivr.com.

[github repository]: https://github.com/dbohdan/classless-css
