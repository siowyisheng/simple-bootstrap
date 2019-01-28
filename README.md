# The Simple Guide to Bootstrap

_Bootstrap 4 explained simply._

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/siowyisheng/simple-bootstrap/blob/master/LICENSE) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

## Table of Contents <!-- omit in toc -->

- [Overview](#overview)
- [Notation](#notation)
- [Installation](#installation)
- [Set basic padding and margins for a div](#set-basic-padding-and-margins-for-a-div)
- [Stack elements on a small screen](#stack-elements-on-a-small-screen)
- [Create media objects (combinations of html elements) for reuse](#create-media-objects-combinations-of-html-elements-for-reuse)
- [Remove default browser list bullets](#remove-default-browser-list-bullets)
- [Hide an element on small/large screens](#hide-an-element-on-smalllarge-screens)
- [Add/remove element margins](#addremove-element-margins)
- [Add/remove element padding](#addremove-element-padding)
- [Center a fixed-width div](#center-a-fixed-width-div)
- [Style subtitles](#style-subtitles)
- [Style large headings](#style-large-headings)
- [Center text](#center-text)
- [Make an inline list (eg. for a navbar)](#make-an-inline-list-eg-for-a-navbar)
- [Make an image responsive to the parent](#make-an-image-responsive-to-the-parent)
- [Style images](#style-images)
- [Align an image](#align-an-image)
- [Make a responsive table](#make-a-responsive-table)
- [Add div borders](#add-div-borders)
- [Float multiple elements within the same block](#float-multiple-elements-within-the-same-block)
- [Make a "close" icon](#make-a-close-icon)
- [Style text colors](#style-text-colors)
- [Set background color](#set-background-color)
- [Set div width as percentage](#set-div-width-as-percentage)
- [Remove the default underlines from links](#remove-the-default-underlines-from-links)
- [23 components](#23-components)
- [Jumbotron](#jumbotron)
- [Navbar](#navbar)
- [Breadcrumb](#breadcrumb)
- [Button](#button)
- [Button group](#button-group)
- [Card](#card)
- [Carousel](#carousel)
- [Collapse/accordion](#collapseaccordion)

## Overview

Build your website quickly using **components**, then **format and lay them out**, all by giving html elements specific classes.

## Notation

## Installation

Link the dependencies (jQuery and Popper.js)

```html
<script
  src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
  integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
  crossorigin="anonymous"
></script>
<script
  src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"
  integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49"
  crossorigin="anonymous"
></script>
```

Link the CDN version below or [the downloaded compiled version](https://getbootstrap.com/docs/4.1/getting-started/download/#compiled-css-and-js) within <head>.

```html
<link
  rel="stylesheet"
  href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css"
  integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO"
  crossorigin="anonymous"
/>
<script
  src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"
  integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy"
  crossorigin="anonymous"
></script>
```

## Set basic padding and margins for a div

```html
<div class="container">Your content</div>

<!-- or -->

<div class="container-fluid">Your content</div>
```

## Stack elements on a small screen

Here, the columns will stack on top of each other if the width is below 768px. Otherwise, they will be divided into 3 columns. The numbers in each row add up to 12.

```html
<div class="container">
  <div class="row">
    <div class="col-sm-4">Your content</div>
    <div class="col-sm-4">Your content</div>
    <div class="col-sm-4">Your content</div>
  </div>
</div>
```

## Create media objects (combinations of html elements) for reuse

```html
<div class="media">
  <img src="..." class="mr-3" alt="..." />
  <div class="media-body">
    <h5 class="mt-0">Media heading</h5>
    Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque
    ante sollicitudin. Cras purus odio, vestibulum in vulputate at, tempus
    viverra turpis. Fusce condimentum nunc ac nisi vulputate fringilla. Donec
    lacinia congue felis in faucibus.
  </div>
</div>
```

## Remove default browser list bullets

```html
<ul class="list-unstyled">
  <li>Your content</li>
  <li>Your content</li>
</ul>

<!-- or -->

<ol class="list-unstyled">
  <li>Your content</li>
  <li>Your content</li>
</ol>
```

## Hide an element on small/large screens

```html
<div class="d-none d-sm-block">
  This doesn't appear on small screens narrower than 768px.
</div>

<div class="d-block d-sm-none">
  This doesn't appear on screens 768px and wider.
</div>
```

## Add/remove element margins

You can use 0-5 for different levels of margin.

```html
<!-- add bottom margin -->
<div class="mb-4">Your content</div>

<!-- add right margin -->
<div class="mr-4">Your content</div>

<!-- add bottom margin -->
<div class="mb-0">Your content</div>

<!-- add right margin -->
<div class="mr-0">Your content</div>
```

## Add/remove element padding

You can use 0-5 for different levels of padding.

```html
<!-- add left and right padding -->
<div class="px-4">Your content</div>

<!-- add top and bottom padding -->
<div class="py-4">Your content</div>

<!-- remove left and right padding -->
<div class="px-0">Your content</div>

<!-- remove top and bottom padding -->
<div class="py-0">Your content</div>
```

## Center a fixed-width div

```html
<div class="mx-auto" style="width: 200px;">Centered element</div>
```

## Style subtitles

```html
<p class="lead">Your subtitle</p>
```

## Style large headings

You can use 1-4 (smallest) for different sizes.

```html
<h1 class="display-1">Your large heading</h1>
```

## Center text

```html
<p class="text-center">Your content</p>
```

## Make an inline list (eg. for a navbar)

```html
<ul class="list-inline">
  <li class="list-inline-item">Lorem ipsum</li>
  <li class="list-inline-item">Phasellus iaculis</li>
  <li class="list-inline-item">Nulla volutpat</li>
</ul>
```

## Make an image responsive to the parent

```html
<img src="..." class="img-fluid" alt="Responsive image" />
```

## Style images

```html
<img src="..." class="rounded" alt="Responsive image" />

<!-- or -->

<img src="..." class="rounded-circle" alt="Responsive image" />

<!-- or -->

<img src="..." class="rounded-pill" alt="Responsive image" />
```

## Align an image

```html
<img src="..." class="float-left" alt="..." />

<!-- or -->

<img src="..." class="float-right" alt="..." />

<!-- or -->

<img src="..." class="mx-auto d-block" alt="..." />
```

## Make a responsive table

```html
<div class="table-responsive">
  <table class="table">
    <thead>
      <tr>
        <th>Your table header</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Your table row header</th>
        <td>Your table content</td>
      </tr>
    </tbody>
  </table>
</div>
```

## Add div borders

```html
<div class="border">Your content</div>

<!-- or -->

<div class="border-top">Your content</div>

<!-- or -->

<div class="border-right">Your content</div>
```

## Float multiple elements within the same block

```html
<div class="bg-info clearfix">
  <button type="button" class="btn btn-secondary float-left">
    Example Button floated left
  </button>
  <button type="button" class="btn btn-secondary float-right">
    Example Button floated right
  </button>
</div>
```

## Make a "close" icon

```html
<button type="button" class="close" aria-label="Close">
  <span aria-hidden="true">&times;</span>
</button>
```

## Style text colors

```html
<p class="text-primary">Your text</p>
<p class="text-secondary">Your text</p>
<p class="text-success">Your text</p>
<p class="text-danger">Your text</p>
<p class="text-warning">Your text</p>
<p class="text-info">Your text</p>
<p class="text-muted">Your text</p>
```

## Set background color

```html
<p class="bg-primary text-white">Your text</p>
<p class="bg-secondary text-white">Your text</p>
<p class="bg-success text-white">Your text</p>
<p class="bg-danger text-white">Your text</p>
<p class="bg-warning text-dark">Your text</p>
<p class="bg-info text-white">Your text</p>
<p class="bg-light text-dark">Your text</p>
<p class="bg-dark text-white">Your text</p>
<p class="bg-white text-dark">Your text</p>
```

## Set div width as percentage

```html
<div class="w-25 p-3" style="background-color: #eee;">Width 25%</div>
<div class="w-50 p-3" style="background-color: #eee;">Width 50%</div>
<div class="w-75 p-3" style="background-color: #eee;">Width 75%</div>
<div class="w-100 p-3" style="background-color: #eee;">Width 100%</div>
<div class="w-auto p-3" style="background-color: #eee;">Width auto</div>
```

## Remove the default underlines from links

```html
<a class="text-decoration-none">Your link</a>
```

## 23 components

## Jumbotron

## Navbar

## Breadcrumb

## Button

## Button group

## Card

## Carousel

## Collapse/accordion
