---
weight: 35
title: "1.2.1 The p element"
icon: "work"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
images: []
---

This tutorial guides you through adding a `p` (paragraph) element to a DITA XML topic.

## Overview

By the end of this tutorial, you will be able to:

* Explain the purpose and importance of paragraph elements in DITA XML
* Identify appropriate locations to use paragraph elements in DITA documents
* Add new paragraph elements to a DITA concept document using the Oxygen XML editor
* Apply different methods for inserting paragraph elements in Oxygen
* Create structured paragraph content in DITA XML

## Background

In DITA, a `<p>` element represents a block of text that has a single idea.

Use `<p>` to wrap any block of text that forms a single idea or unit of information. `<p>` elements can appear (almost) anywhere you need body text. For example: inside the main content area, within list items, notes, or table entries.

`<p>` is a *block* element.

## Add a `<p>` element

1. Open the concept topic you edited in [The shortdesc element](./shortdesc.md).
2. Click between the closing `<p>` tag and the closing `<conbody>` tag to place the cursor.
3. Add a new `<p>` element using one of the following methods:

    * In the **Elements** view, locate and double-click `p`.

    ![Elements view > p](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748594773/oxygen-select-p-list.jpg)
    
	* Press <kbd>ENTER</kbd> to display a selection list. Type `p` or select `p` from the list and press <kbd>ENTER</kbd>.
    
	![Select p from context menu](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748594927/oxygen-select-p-menu.jpg)
    
	Oxygen inserts an empty `<p>` element after the first `<p>` element and before the closing `<conbody>` tag.

4. Within the new `<p>` element, type `This is my second paragraph.`.
5. Save the file.
    
### Expected result
![Final document window for this tutorial](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748595136/oxygen-paragraph-tutorial-complete.jpg)

{{< alert context="success" text="Refer to the file `DITA_101_oXygen/my_concept_using_paragraphs.xml` to confirm the successful completion of this task." />}}