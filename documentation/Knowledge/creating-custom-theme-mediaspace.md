---
layout: page
title: "Creating a Custom Theme for MediaSpace"
date: 2013-02-10 15:40:24
---

In Kaltura MediaSpace, you can create themes to override the generic view scripts of the application.

<div class="tabItem">
  <p>
    A custom theme can override some or all of the generic view scripts of MediaSpace. A view script that is not implemented in the custom theme will be taken from the generic view scripts.
  </p>
  
  <p>
    A theme includes two sets of folders, as follows:
  </p>
  
  <pre>{mediaspace install path}/
           themesCustom/
              {custom theme folder}
           public/themesCustom
              {custom theme folder}</pre>
  
  <p>
    Under the MediaSpace Installation path, all of the custom themes that you want to overiride should be in the main themes folder.
  </p>
  
  <p>
    Under the main themes folder (below mediaspace installation path) should be implemented all the different view scripts that a custom theme wishes to override
  </p>
  
  <p>
    All of the theme assets (images, css files and javascript files) that are accessible to the web should be placed in the public/themes folder.
  </p>The folder structure of a theme should reflect the same folder structure of the different views and layouts scripts.
  
  <pre>{themename}/views/scripts/
{themename}/views/scripts/playlist/
{themename}/views/scripts/install/
{themename}/views/scripts/redirector/
{themename}/views/scripts/partials/
{themename}/views/scripts/partials/mymedia/
{themename}/views/scripts/partials/upload/
{themename}/views/scripts/partials/myplaylists/
{themename}/views/scripts/partials/admin/
{themename}/views/scripts/partials/channels/
{themename}/views/scripts/partials/entryItem/
{themename}/views/scripts/partials/widgets/
{themename}/views/scripts/category/
{themename}/views/scripts/channels/
{themename}/views/scripts/gallery/
{themename}/views/scripts/error/
{themename}/views/scripts/user/
{themename}/views/scripts/index/
{themename}/views/scripts/entry/
{themename}/layouts/scripts/
        </pre>
  
  <p>
    In addition, a theme can also override view scripts of the different modules.
  </p>
  
  <p>
    Refer to list of view scripts available in MediaSpace.
  </p>
</div>

<h3 class="tabItem">
  <span style="font-size: 1.17em;">Info file</span>
</h3>

Themes can include an optional file called theme.info, containing a short description of the theme.

<pre>{themename}/theme.info</pre>

### Dark / Light Theme for the Header

This is set through the MediaSpace admin (in the ‘Header’ menu, under header style).

### Modifying the CSS:

From your MediaSpace root folder location, go to a folder named ‘themesCustom’, and create a new folder. The new folder name will be the name of the new theme.

In Unix, the commands would be:

<pre>&gt;cd mediaspace_v4<span style="color: #ff0000;">(version number)</span></pre>

<pre>&gt;cd themesCustom</pre>

<pre>&gt;mkdir themename</pre>

Go back to the MediaSpace root folder, and into:  ‘<span style="font-size: 10px;">public/themesCustom</span>

Create a new folder with the same name:

<pre>&gt;cd ..</pre>

<pre>&gt;cd public/themesCustom</pre>

<pre>&gt;mkdir themename</pre>

Go to the newly created folder, and create a folder named: ‘css’. In the ‘css’ folder, create a file named: ‘theme.css’.

<pre>&gt;cd themename</pre>

<pre>&gt;mkdir css</pre>

<pre>&gt;cd css</pre>

This file will override MediaSpaces’s default css, once you change the theme in the MediaSpace admin - to the newly created folder (In the ‘Application’ tab):<span style="font-size: 10px;"> </span>

<p class="Default">
  Use Firebug (or a similar tool) to find the CSS selector which is already being used to create the existing look. Use the exact same selector in the theme.css file.
</p>

Example for theme.css file content:

<pre>body {&nbsp;&nbsp;&nbsp;&nbsp;</pre>

<pre>&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; color: #000099;</pre>

<pre>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; background-color: #dddddd;</pre>

<pre>&nbsp;&nbsp;&nbsp; &nbsp; }</pre>

###  Modifying Buttons and Icons

Replace the images/ 'sprite' – that are in: [MediaSpace folder]\public\img with your custom images / sprites.

<p class="Default">
  <strong>  </strong>
</p>