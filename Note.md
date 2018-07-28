# mmatplotlib.pyplot
- import the moodule

~~~

- import matplotlib.pyplot as plt

~~~
-----------

## plot()
- plot(*args, **kwargs)
  - plot([x],y,[fmt], data= NOne,**kwargs)
  - plot([x], y, [fmt], [x2], y2, [fmt2], ..., **kwargs)

--------------

- You can use Line2D properties as keyword arguments for more control on the appearance.
Line properties and fmt can be mixed. The following two calls yield identical results

-'go--' as same as  color='green', marker='o', linestyle='dashed'

~~~~

>>> plot(x, y, 'go--', linewidth=2, markersize=12)
>>> plot(x, y, color='green', marker='o', linestyle='dashed',
        linewidth=2, markersize=12)
        
~~~~


---------------

- **Plotting labelled data**

All indexable objects are supported. This could e.g. be a dict, a pandas.DataFame or a structured numpy array
~~~~

obj={'xlabel':[1,2,3,4],'ylabel':[1,2,3,4]}

plot('xlabel', 'ylabel', data=obj)

~~~~



--------------

- **multiple sets of data**

  1. using plot() multiple times 
  pyplot 对于这个对象 相当于 plot() 就是一次绘制
  ~~~

  >>> plot([1,2,3,4],[3,4,None,None],'g')

  >>> plot([1,2,3,4,5,6],[1,4,None,None,5,6],'r')
  ~~~
  
  --------------
  
  2. given lable __x__  x=[a,b,c,d] then pass 4Y __ya,yb,yc,yd__ Y=[ya=[..],yb=[..],yc=[..],yd=[..]]
  
  ~~~
  
  >>> a =[['a','b','c','d'],[1,2,3,4],[2,3,4,5],[3,4,5,6],[4,5,6,7]]
  >>> plot(a[0], a[1:])
  
  ~~~
  
  <img width="300" height="300" src="/img1.png"/>
  
  ----------
  3. multiple sets of arguments
  ~~~
  
  >>> plot(x1, y1, 'g^', x2, y2, 'g-')
  
  ~~~
  --------
  当绘制多条线时 默认会不同颜色
  By default, each line is assigned a different style specified by a ‘style cycle’. The fmt and line property parameters are only necessary if you want explicit deviations from these defaults. Alternatively, you can also change the style cycle using the ‘axes.prop_cycle’ rcParam.
  
 ----------
### Format
 ~~~
 fmt='[color][marker][line]'
 ~~~
 
 

### detail doc : [matplotlib.plot](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.plot.html#matplotlib.pyplot.plot)

