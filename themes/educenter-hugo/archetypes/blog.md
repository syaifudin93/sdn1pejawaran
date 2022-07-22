---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
# page title background image
bg_image: "images/backgrounds/page-title.jpg"
# meta description
description : ""
# post thumbnail
image: "images/blog/post-{{ .Name }}.jpg"
# post author
author: ""
# taxonomy
categories: [""]
tags: ["", ""]
# type
type: "post"
slug: "blog-post-{{ .Name }}"

---

**Insert Lead paragraph here.**

## New Cool Posts

{{ range first 10 ( where .Site.RegularPages "Type" "cool" ) }}
* {{ .Title }}
{{ end }}