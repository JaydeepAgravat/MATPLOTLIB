# [MATPLOTLIB](https://github.com/JaydeepAgravat/MATPLOTLIB/blob/main/MATPLOTLIB.ipynb)

## TOPIC

- 2D Line plot
- Scatter Plots
- Bar Chart
- Histogram
- Pie Chart
- Changing styles
- Save figure
- Colored Scatterplots
- Annotations
- Horizontal and Vertical lines
- Subplots
- 3D Scatter Plots
- 3D Line Plot
- 3D Surface Plots
- Contour Plots
- Heatmap
- Pandas Plot()

## REMARK ABOUT MATPLOTLIB

```python
plt.plot(
    x,y,
    color='',
    linestyle='',
    linewidth='',
    marker='',
    markersize='',
    label=''
)
plt.title('')
plt.xlabel('')
plt.ylabel('')
plt.xticks(rotation='vertical')
plt.xlim()
plt.ylim()
plt.legend(loc='upper left')
plt.grid()
plt.show()
```

```python
plt.scatter(
    x,y,
    s=
)

plt.bar(
    x,y,
    color=
)

plt.hist(
    x,
    bins=
)

plt.pie(
    x,
    labels=,
    autopct='%0.1f%%'
    explode=
    shadow=True
)
```

```python
plt.style.available
plt.style.use('ggplot')
plt.savefig('test.png')
plt.figure(figsize=(15, 7))
```

```python
plt.scatter(
    x,y,
    c=,
    cmap='jet',
    alpha=0.7
)

plt.colorbar()

plt.text(
    x,y,
    'name',
    fontdict={'size':12,'color':'brown'}
)

plt.axhline(140,color='green')
plt.axvline(30,color='red')

```

```python
fig, ax = plt.subplots(nrows=2,ncols=2,figsize=(10,10))

ax[0,0].scatter(bt['avg'],bt['strike_rate'],color='red')
ax[0,1].scatter(bt['avg'],bt['runs'])
ax[1,0].hist(bt['avg'])
ax[1,1].hist(bt['runs'])
plt.show()
```

```python
fig = plt.figure()

ax1 = fig.add_subplot(2,2,1)
ax1.scatter(bt['avg'],bt['strike_rate'],color='red')

ax2 = fig.add_subplot(2,2,2)
ax2.hist(bt['runs'])

ax3 = fig.add_subplot(2,2,3)
ax3.hist(bt['avg'])

plt.show()
```

```python
fig = plt.figure()
ax = plt.subplot(projection='3d')

ax.scatter3D(bt['runs'],bt['avg'],bt['strike_rate'],marker='+')
ax.set_title('IPL batsman analysis')
ax.set_xlabel('Runs')
ax.set_ylabel('Avg')
ax.set_zlabel('SR')

plt.show()
```

```python
x = [0,1,5,25]
y = [0,10,13,0]
z = [0,13,20,9]

fig = plt.figure()

ax = plt.subplot(projection='3d')

ax.scatter3D(x,y,z,s=[100,100,100,100])
ax.plot3D(x,y,z,color='red')

plt.show()
```

```python
fig = plt.figure(figsize=(12,8))

ax = plt.subplot(projection='3d')

p = ax.plot_surface(xx,yy,z,cmap='viridis')
fig.colorbar(p)
plt.show()
```

```python
fig = plt.figure(figsize=(12,8))

ax = plt.subplot()

p = ax.contour(xx,yy,z,cmap='viridis')
p = ax.contourf(xx,yy,z,cmap='viridis')
fig.colorbar(p)
plt.show()
```

```python
plt.figure(figsize=(20,10))
plt.imshow(grid)
plt.yticks(delivery['overs'].unique(), list(range(1,21)))
plt.xticks(np.arange(0,6), list(range(1,7)))
plt.colorbar()
plt.grid()
plt.show()
```

```python
df.plot(
    kind=,
)
plt.show()
```
