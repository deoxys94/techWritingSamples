---
weight: 25
title: "1.2 Introduction to DITA elements"
icon: "work"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
images: []
---

DITA provides a large variety of elements, represented as tags, for use across multiple topic types. You don't need to know every tag to author using DITA XML. 

The following table describes the basic DITA XML element categories.

<table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Block-level elements</td>
      <td>
        <p>A block-level element always starts on a new line. Oxygen always adds a margin before and after the element.</p>
        <p>You don't need to wrap block-level elements with &lt;p> tags, they can exist on their own.</p>
        <p>Examples include:</p>
        <ul>
          <li>
            <p><code>&lt;p&gt;</code></p>
          </li>
          <li>
            <p><code>&lt;title&gt;</code></p>
          </li>
          <li>
            <p><code>&lt;shortdesc&gt;</code></p>
          </li>
          <li>
            <p><code>&lt;note&gt;</code></p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Inline elements</td>
      <td>
        <p>Inline elements are the opposite of block-level elements:</p>
        <ul>
          <li>
            <p>They don't start in a new line.</p>
          </li>
          <li>
            <p>You must wrap them in other tags (like &lt;p> tags).</p>
          </li>
        </ul>
        <p>Examples include:</p>
        <ul>
          <li>
            <p><code>&lt;menucascade&gt;</code></p>
          </li>
          <li>
            <p><code>&lt;uicontrol&gt;</code></p>
          </li>
          <li>
            <p><code>&lt;codeph&gt;</code></p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>