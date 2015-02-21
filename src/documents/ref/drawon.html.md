---
title: drawon
description: for drawing on a Sprite
layout: reference
section: animation
refOrder: 6
---

`drawon` is used to draw on another Turtle or Sprite.
It can be used to create your own turtle shapes.

<h3>Drawing a sprite with drawon</h3>

A turtle `t` or other element can draw on Sprite `s` by
saying `t.drawon s`.

<pre class="jumbo">
s = new Sprite
  color: gray
t = new Turtle
t.drawon s
t.dot red, 100
t.pen blue, 10
t.fd 100
t.pen null
t.ht()
t.drawon window
s.lt 90
s.fd 200
</pre>

After you are done drawing, you can say `drawon window`
to go back to drawing on the main window.  This will
also cause the sprite being drawn on to wait until
the drawing is done before moving.

Be sure to wait for the drawing to finish before you
start moving the Sprite that is being drawn.  You
can do this by drawing at `t.speed Infinity` or by
using `sync` to synchronize the objects.
