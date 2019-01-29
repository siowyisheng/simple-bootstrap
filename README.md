# The Simple Guide to Bootstrap

_Bootstrap 4 explained simply._

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/siowyisheng/simple-bootstrap/blob/master/LICENSE) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

## Table of Contents <!-- omit in toc -->

- [Foreward](#foreward)
- [Overview](#overview)
- [Installation](#installation)
- [Components](#components)
  - [Content layout](#content-layout)
  - [User interaction](#user-interaction)
  - [Navigation](#navigation)
  - [Notifications](#notifications)
- [Layout and Format](#layout-and-format)
  - [Alignment](#alignment)
  - [Spacing](#spacing)
  - [Mobile responsiveness](#mobile-responsiveness)
  - [Styling](#styling)

## Foreward

This opinionated guide omits components which are easily executed without bootstrap, and focuses on the perceived most common use cases. Be sure to refer to [the official documentation](https://getbootstrap.com/docs/4.2/getting-started/introduction/) for greater detail.

## Overview

Build your website quickly using **components**, then **format and lay them out**, all by giving html elements specific classes.

## Installation

The easiest installation is via CDN. Just include the below in your HTML.

```html
<head>
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css"
    integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS"
    crossorigin="anonymous"
  />
  Other elements...
</head>
<body>
  Your elements...
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
  <script
    src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"
    integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy"
    crossorigin="anonymous"
  ></script>
</body>
```

Alternatively, you can [install the necessary files locally](https://getbootstrap.com/docs/4.2/getting-started/download/).

## Components

### Content layout

#### Card

General purpose content containers

#### Jumbotron

Singular component with key marketing message (probably on homeview).

#### Carousel

Collection of cycle-able images

#### Collapse

Toggle visibility of large elements

#### List group

Show list content

#### Media object

Highly-repetitive, nestable component.

#### Modal

Important content allowing easy return to the current page.

### User interaction

#### Forms

Get input from the user.

#### Buttons

Target areas for actions in forms or dialogs.

#### Button group

Groups of related buttons.

#### Alerts

Feedback messages to user actions.

### Navigation

#### Navbar

Navigation bar

#### Scrollspy

Show active section on a fixed navbar

#### Breadcrumb

Current page location within the site's structure.

### Notifications

#### Badge

Labels and notification counts

#### Toasts

Notifications

#### Tooltips

Extra information on certain terms/concepts

## Layout and Format

### Alignment

#### Center a fixed-width div

```html
<div class="mx-auto" style="width: 200px;">Centered element</div>
```

#### Center text

```html
<p class="text-center">Your content</p>
```

#### Float multiple elements within the same block

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

#### Align an image

```html
<img src="..." class="float-left" alt="..." />

<!-- or -->

<img src="..." class="float-right" alt="..." />

<!-- or -->

<img src="..." class="mx-auto d-block" alt="..." />
```

### Spacing

#### Set basic padding and margins for a div

```html
<div class="container">Your content</div>

<!-- or -->

<div class="container-fluid">Your content</div>
```

#### Add/remove element margins

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

#### Add/remove element padding

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

### Mobile responsiveness

#### Hide an element on small/large screens

```html
<div class="d-none d-sm-block">
  This doesn't appear on small screens narrower than 768px.
</div>

<div class="d-block d-sm-none">
  This doesn't appear on screens 768px and wider.
</div>
```

#### Stack elements on a small screen

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

#### Make an image responsive to the parent

```html
<img src="..." class="img-fluid" alt="Responsive image" />
```

#### Make a responsive table

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

### Styling

#### Remove default browser list bullets

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

#### Remove the default underlines from links

```html
<a class="text-decoration-none">Your link</a>
```

#### Style images

```html
<img src="..." class="rounded" alt="Responsive image" />

<!-- or -->

<img src="..." class="rounded-circle" alt="Responsive image" />

<!-- or -->

<img src="..." class="rounded-pill" alt="Responsive image" />
```

#### Style text colors

```html
<p class="text-primary">Your text</p>
<p class="text-secondary">Your text</p>
<p class="text-success">Your text</p>
<p class="text-danger">Your text</p>
<p class="text-warning">Your text</p>
<p class="text-info">Your text</p>
<p class="text-muted">Your text</p>
```

#### Set background color

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

#### Style subtitles

```html
<p class="lead">Your subtitle</p>
```

#### Style large headings

You can use 1-4 (smallest) for different sizes.

```html
<h1 class="display-1">Your large heading</h1>
```

#### Add div borders

```html
<div class="border">Your content</div>

<!-- or -->

<div class="border-top">Your content</div>

<!-- or -->

<div class="border-right">Your content</div>
```
