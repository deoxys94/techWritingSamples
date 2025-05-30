---
weight: 40
title: "1.2.2 The codeph element"
icon: "code"
date: "2025-05-05T10:00:00+08:00"
lastmod: "2025-05-05T10:00:00+08:00"
draft: false
toc: true
images: []
---

This tutorial guides you through adding a `codeph` (code phrase) element to a DITA XML topic.

## Overview

By the end of this tutorial, you will be able to:

*   Explain the purpose and usage of code phrase elements in DITA XML.
*   Identify appropriate locations to use `codeph` elements in DITA documents.
*   Add new `codeph` elements to a DITA concept document using the Oxygen XML editor.
*   Apply different methods for inserting `codeph` elements in Oxygen.
*   Mark up inline code snippets and programming terms in DITA XML.

## Background

In DITA, a `<codeph>` element represents an inline phrase of code. It's used to semantically identify small pieces of computer code that appear within the flow of text. Common uses include marking up:

*   Variable names (e.g., `<codeph>maxConnections</codeph>`)
*   Function or method names (e.g., `<codeph>calculateTotal()</codeph>`)
*   Command names (e.g., run `<codeph>npm install</codeph>`)
*   Filenames or paths (e.g., open `<codeph>src/main.js</codeph>`)
*   Short code snippets or keywords that fit naturally within a sentence (e.g., the `<codeph>public static void</codeph>` declaration).

Use `<codeph>` to wrap these code phrases directly a paragraph (`<p>`).

`<codeph>` is an *inline* element. 

## Add a `<codeph>` element

1. Open the concept topic you edited in [The p element](./paragraph.md).
2. Click between the closing `<p>` tag and the closing `<conbody>` tag to place the cursor.
3. Add a new `<p>` element.
4. Type the following text inside the new `<p>` element: `A paragraph in text mode looks like this: `

   Ensure to leave a space after the colon.

5.  Add a new `<codeph>` element.
6. Type the following inside the `<codeph>` element: `<p>Hello</p>`
5.  Save the file.

### Expected result
> ![Result of the codeph tutorial](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748596652/codeph-result_aosxq0.png)

{{< alert context="success" text="Refer to the file `DITA_101_oXygen/my_concept_using_codeph.xml` (or a similar name you chose) to confirm the successful completion of this task." />}}