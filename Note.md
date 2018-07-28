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
  
  



