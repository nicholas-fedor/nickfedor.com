---
title: "{{ title (replace (replaceRE `^[0-9]+-` `` .File.ContentBaseName) `-` ` `) }}"
date: {{ time.Now.Format "2006-01-02" }}
draft: true
slug: "{{ replaceRE `^[0-9]+-` `` .File.ContentBaseName }}"
banner: ""
---
