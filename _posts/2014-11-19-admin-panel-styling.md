---
layout: page
title: "Admin Panel Styling"
category: ref
date: 2014-11-19 15:03:29
---

Conductor uses the [AdminLTE theme](http://almsaeedstudio.com/AdminLTE/) which is based off [Bootstrap 3](http://getbootstrap.com/). As such, all components from 
AdminLTE and Bootstrap 3 will be available in your admin views.

###Examples###

Basic header

```
<h4 class="page-header">
    Widget Areas
    <small>Define your widget areas here</small>
</h4>
```

Content box with a form

```
<div class="box box-solid box-primary">
    <div class="box-header">
        <h4 class="box-title">New Area</h4>
    </div>
    <div class="box-body">
        <form>
            <div class="form-group">
                <label for="name">Name</label>
                <input type="text" class="form-control" />
            </div>
            <div class="form-group">
                <label for="slug">Slug</label>
                <input type="text" class="form-control" disabled />
            </div>
        </form>
    </div>
    <div class="box-footer">
        <button class="btn btn-primary btn-small">Save</button>
        <button class="btn btn-danger btn-small">Delete</button>
    </div>
</div>
```
