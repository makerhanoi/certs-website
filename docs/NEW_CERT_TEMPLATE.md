# Create new certificate template

## 1. Prepare template file

Prepare a certificate SVG file as a template in `themes/certtheme/layouts/partials/cert_templates`.

- Open SVG file in VS Code, remove header:

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
```

- Modify the file with [Inkscape](https://inkscape.org/) to add place holders with following values: 
    - `{{ .Params.name }}` : full name of cerified person
    - `{{ .Params.reason }}` : purpose of the cerificate
    - `{{ .Params.issue_date }}` : issue date
    - `{{ .Params.undersigned }}` : name under signature
    - Add an image with URL (Right click > Image Properties > URL) is set to `{{ .Params.signature }}`


## 2. Apply the theme

- Create a new certificate from sample file at `content/certificates/vsu_2021/nguyen-viet-anh.md`, and set `theme` to the template file name.

```
---
title: Nguyen Viet Anh
date: 2022-03-26
categories: ["Certification"]
tags: ["VSU"]
slug: "/certs/vsu_2021/nguyen-viet-anh"
name: "Nguyen Viet Anh"
reason: "for completion of VSU Robotics Course 2022"
issue_date: "26/03/2022"
signature: "/signatures/tuanle.png"
undersigned: "Tuan Le - Founder MakerViet"
theme: "theme1.svg"
---
```
