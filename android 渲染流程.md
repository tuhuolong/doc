```
measure    (first|layoutRequest)   (main thread)
    onMeasure
    setMeasuredDimension
```

```
layout     (first|layoutRequest)   (main thread)
    setFrame
    onLayout
```

```
draw       (dirty|animation)       (main thread)  -> display list
    drawBackground
    onDraw            (自身)
    dispatchDraw      (子view)
    onDrawScrollBars
```

```
sync                               (render thread)
```

```
process   (display list)           (render thread): draw command--opengl api-->gpu command
```

```
send and wait (glFlush/glFinish)   (render thread) driver : send gpu command buffer->gpu command queue (render thread blocked)
```

```
execute                            (gpu) : render thread blocked
```

```
swap buffer   (glSwapBuffers)      (render thread) -> (surfaceflinger)
```

```
composition                        (surfaceflinger)
```



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
[深入了解Android Graphics Pipeline](https://github.com/bboyfeiyu/android-tech-frontier/tree/master/androidweekly/%E6%B7%B1%E5%85%A5%E4%BA%86%E8%A7%A3Android%20Graphics%20Pipeline-part-1 "深入了解Android Graphics Pipeline")
<br>
[Let's talk about eglMakeCurrent, eglSwapBuffers, glFlush, glFinish](https://katatunix.wordpress.com/2014/09/17/lets-talk-about-eglmakecurrent-eglswapbuffers-glflush-glfinish/)
<br>
[OpenGL Synchronization](https://www.opengl.org/wiki/Synchronization)
<br>
<br>