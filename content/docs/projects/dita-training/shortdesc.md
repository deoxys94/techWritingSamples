---
weight: 30
title: "1.2.1 The shortdesc element"
icon: "work"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
images: []
---

This tutorial guides you through adding a `<shortdesc>` (short description) element to a DITA XML topic.

## Overview

By the end of this tutorial, you will be able to:

- Explain the purpose and importance of the `<shortdesc>` element in DITA topics
- Add a `<shortdesc>` element to a DITA concept topic using multiple methods in oXygen XML editor
- Write effective short descriptions that accurately summarize topic content
- Position the `<shortdesc>` element correctly within the DITA topic structure

## Background

The `<shortdesc>` element provides a brief description of the purpose or theme of the topic. Text within the <shortdesc> element:

- Appears as tooltips in online help systems
- Functions as link previews in search engine results

`<shortdesc>` is a *block* element.

## Add a `<shortdesc>` element

1. Open the concept topic you created in [Create a concept topic](./create-concept-topic.md).
2. Click to the right of the closing `<title>` tag to place the cursor.
3. Add a `<shortdesc>` element by using one of the following methods:

    * In the **Elements** view, locate and double-click **shortdesc**.

    ![Elements view > Shortdesc](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748593542/elements-shortdesc_unekag.png)

    * Press <kbd>ENTER</kbd> to display a selection list. Type `shortdesc` or select **shortdesc** from the list and press <kbd>ENTER</kbd>.

    ![Select shortdesc from context menu](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748593733/menu-shortdesc_kgbgra.png)

    Oxygen inserts an empty `<shortdesc>` element after the topic title.

4. Click to place the cursor between the opening and closing `<shortdesc>` tags.
5. Type: `Create a <concept> topic to provide information about a particular subject.`
6. Save the file.

### Expected result

> ![Expected result](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748594149/shortdesc-tutorial-complete.jpg)

{{< alert context="success" text="Refer to the file `DITA_101_oXygen/my_concept_shortdesc.xml` to confirm the successful completion of this task." />}}