---
weight: 20
title: "1.1 Concept topics"
icon: "work"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
images: []
---

This tutorial guides you through creating your first concept topic using DITA XML.

## Overview

By the end of this tutorial, you will be able to:

- Create a new DITA concept topic using the built-in templates
- Save an XML file with appropriate naming conventions
- Modify the default title element in a concept topic
- Apply proper paragraph formatting to body text in DITA
- Identify the basic structure of a DITA concept document

## Background

Concepts give conceptual or descriptive information about a thing, a product or a process. Concepts help readers understand essential ideas, terms, products, processes, or any descriptive information they need before doing tasks or understanding reference material.

A concept is similar to an encyclopedia entry and provides more detail than a reference topic, which is similar to a dictionary entry.

## When should I use a concept topic?

Use a concept topic when you need to give explanations, definitions, or overview information. This type of topic is ideal for introducing a product, explaining a process, defining key terms, or describing how something works.

{{% alert icon="💡" context="info" %}}

**Tip**

A concept topic usually answers the following questions:
* What is this?
* What does this do?
* How does this work?
* Why is this important?

{{% /alert %}}

## Create a concept topic

1.  Go to **File** > **New** or click the **New...** (![New File Icon](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748585695/new-file-icon-dark_rm4gwk.png)) icon.

2.  In the folder structure, click **Popular** > **DITA** > **Topics** > **Concept**.

    ![Templates Oxygen New File](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748585802/oxygen-template-selector_zmetyg.png)

3.  Click **Create** to create a new concept with the default elements.

    ![New Concept](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748585936/oxygen-new-concept_rd0qvl.jpg)

4.  Go to **File** > **Save**

5.  For the file name, follow the existing naming convention:
    1. Choose a descriptive name for your file, for example *my-first-concept*
        
		File names must not include spaces. The only allowed special characters are: `( ) - = _ `
    2. Go to [www.uuidgenerator.net](https://www.uuidgenerator.net/guid) in your browser to generate a GUID.
    3. Copy the generated GUID.
    4. Name your file using the format: `[descriptive-name]=[UUID].xml`

        For example: `my-first-concept=3fa85f64-5717-4562-b3fc-2c963f66afa6.xml`

6.  Change the `<title>` element text to *Hello World*.

7.  Click between the opening `<p>` tag and closing `<p>` tag and type the following: *Always wrap body text in paragraph tags.*

8.  Save the file.

### Expected result

> ![Expected result](https://res.cloudinary.com/dttfzpzjn/image/upload/v1748586099/first-concept-complete_o8sx01.png)

{{< alert context="success" text="Refer to the file `DITA_101_oXygen/my_concept_create.xml` to confirm the successful completion of this task." />}}