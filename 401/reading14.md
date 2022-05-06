# [Matplotlib](https://www.labri.fr/perso/nrougier/teaching/matplotlib/)

matplotlib is a powerful tool used by python for 2d graphics, as it provides a quick way to visualize data and publication quality figures in many formats.

pyplot provides a convenient interface to the matplotlib obj-oriented lib. 

## Simple Plotting

`.plot()` is a handy tool for sharing a vizualization for data/ 

By default plot assumes a y axis, so you typically need to feed it x,y. 

You can also control line properties by using keyword args like linewidth. 

|Property|Value Type|
|:--|:---:|
|alpha |	float|
|animated |	[True or False]|
|antialiased or aa |	[True or False]|
|clip_on |	[True or False]|
|clip_path |	a Path instance and a Transform instance, a Patch|
|color or c |	any matplotlib color|
|contains |	the hit testing function|
|data 	|(np.array xdata, np.array ydata)|
|figure |	a matplotlib.figure.Figure instance|
|label |	any string|
|linewidth or lw |	float value in points

linestyle or ls - `[ '-' | '--' | '-.' | ':' | 'steps' | ...]`

You can customize matplotlib

You can make your style known to Matplotlib by placing your <style-name>.mplstyle file into mpl_configdir/stylelib. You can then load your custom style sheet with a call to style.use(<style-name>). By default mpl_configdir should be ~/.config/matplotlib, but you can check where yours is with matplotlib.get_configdir(); you may need to create this directory. 

```py
# Example
axes.titlesize : 24
axes.labelsize : 20
lines.linewidth : 3
lines.markersize : 10
xtick.labelsize : 16
ytick.labelsize : 16
```

Through the use of commands such as `xlim()` and `ylim()` you can set limits to diplayed data

You can also adjust the ticks for the table. 

Spines which are the lines connecting the axis ticks and noting boundaries. 

```py
ax = plt.gca()
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
```

You can also add legends to the graphs

```py
plt.legend(loc='upper left', frameon=False)
```

## Types of plots

Bar - Note: Need to take care of text alignment

Contour - Note: You need to use clabel command.

Imshow - note: You need to take care of the origin of the image in the imshow command and use a colorbar.

Piechart - Note: You need to modify Z

Quiver Plots - Note: You need to ddraw arrows twice

Polar Axis - Note: You only need to modify the axes

Be sure to check the docs for LineTypes, and Colormaps

### Things I would like to know more about: 

Could matplotlib be used to create actual animated graphics that aren't geometrical such as making pixel art that moves. 