### Gabriel Kuykendall

#### Project 2
I wanted to look at the changes in Howard County over the last fifty years. I grew up in Howard County so I was interest in the development of parks, I believe growth in the number public parks is a sign of the growth of suburbs. Howard County is geared towards families because of their school system and general environment. I decided to cut off at the 1980s and to watch each decade after because the number of parks were low and would provide little expansion during the 10 year periods. The 1980s and 1990s showed the most expansion in parks. Howard County's population increased 91% in the 1980s and 58% in the 1990s, backing up my claim.
I used data from Howard Counties public GIS portal, I manipulated the data in SQL by sorting by year deeded descending and deleting parks without time information, I then selected the FID, year deeded, name, and geometry information to create a new shapefile for the parks. From there I used SQL to select my parameters for each year set. I then used python to load the layers and colors.
##### Change Over Time
![alt text](https://github.com/gkuykendall96/gkuykendall96.github.io/blob/master/gifall.gif)
##### Maps
![alt text](https://github.com/gkuykendall96/gkuykendall96.github.io/blob/master/project2/pre80.png)
![alt text](https://github.com/gkuykendall96/gkuykendall96.github.io/blob/master/project2/80s.png)
![alt text](https://github.com/gkuykendall96/gkuykendall96.github.io/blob/master/project2/90s.png)
![alt text](https://github.com/gkuykendall96/gkuykendall96.github.io/blob/master/project2/2000s.png)

##### Python

    from PyQt5.QtGui import QColor
    from PyQt5.QtCore import Qt
    #load county lines
    hoco = QgsVectorLayer('C:/Users/Admin/Documents/Project2/County_ShapePolygon','Howard_County','ogr')
    if hoco.isValid():
      QgsProject.instance().addmaplayer(hoco)
    renderer = layer.renderer()
    symbol = renderer.symbol()
    symbol.setColor(Qcolor('#ffffb3'))
    layer.triggerRepaint()
    iface.layerTreeView().refreshLayerSymbology(layer.id())
    #load before 80s
    pre = QgsVectorLayer('C:/Users/Admin/Documents/Project2/pre80','Prior_To_1980s','ogr')
    if pre.isValid():
      QgsProject.instance().addmaplayer(pre)
    renderer = layer.renderer()
    symbol = renderer.symbol()
    symbol.setColor(Qcolor('#b7484b'))
    layer.triggerRepaint()
    layerTreeView().refreshLayerSymbology(layer.id())
    #load 80s
    eighty = QgsVectorLayer('C:/Users/Admin/Documents/Project2/80s','1980-1989','ogr')
    if eighty.isValid():
      QgsProject.instance().addmaplayer(eighty)
     renderer = layer.renderer()
     symbol = renderer.symbol()
    symbol.setColor(Qcolor('#e77148'))
    layer.triggerRepaint()
    iface.layerTreeView().refreshLayerSymbology(layer.id()) 
    #load 90s
    ninety = QgsVectorLayer('C:/Users/Admin/Documents/Project2/90s','ninety','ogr')
    if ninety.isValid():
        QgsProject.instance().addmaplayer(ninety)
    renderer = layer.renderer()
    symbol = renderer.symbol()
    symbol.setColor(Qcolor('#987db7'))
    layer.triggerRepaint()
    iface.layerTreeView().refreshLayerSymbology(layer.id())
    #load 2000s to now
    current = QgsVectorLayer('C:/Users/Admin/Documents/Project2/2000s','2000-Present','ogr')
    if current.isValid():
        QgsProject.instance().addmaplayer(current)
    renderer = layer.renderer()
    symbol = renderer.symbol()
    symbol.setColor(Qcolor('#becf50'))
    layer.triggerRepaint()
    iface.layerTreeView().refreshLayerSymbology(layer.id())
