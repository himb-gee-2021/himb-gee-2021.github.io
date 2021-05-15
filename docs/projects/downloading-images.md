# **Downloading Planet Images**
You can download images from Planet using a couple of methods, including but not limited to Planet Explorer or using a client to make requests to the Data API and downloading imagery.

### **Planet Explorer**
Planet Explorer is probably one of the most useful and beloved interface to interact with and download Planet Labs satellite imagery. Not only does it allow you to filter your images to specific sensors but it also allows you to filter by cloud cover among other things. A neat little trick in Planet Explorer is that once the images are filtered if you want to download multiple images at once in an order you can hold down the control key(if using a windows machine) and click on multiple sets of imagery adding them to the same order.

![Using the Planet Explorer](../images/downloading_images.gif)

<center>_Steps to get satellite imagery from Planet Explorer_</center>

Once the images have been ordered sit back and relax as the order notification that your delivery is ready to be picked up will be emailed to you.

To interact with the **Data API** and batch download imagery there is [host of Planet Platform documentation](https://www.planet.com/docs/) that teach you how to do that step by step.

### **Batch Download Images**

#### Using Planet Python CLI
This is the default command line tool that is provided by planet and you can [find the project here](https://github.com/planetlabs/planet-client-python) and it connects to Data API to perform multiple operations such as quick search, activate and download assets among a few other things. Install it easily using

 <center>
```
 pip install planet
```
</center>

 follow it by ```planet init``` to initialize and you are ready to go.

 A simple setup to download images using a geometry(a simple geometry geojson file) and date range (let us say between 2018-07-01 to 2018-08-31), cloud cover(less than 10% or less than 0.1)  could be achieved in a single line of cli command


```
planet data download --item-type PSScene4Band --geom "full path to geometry.geojson" --date acquired gt 2018-07-01 --date acquired lt 2018-08-31 --range cloud_cover lt 0.1 --asset-type analytic --dest "your local directory path"
```

#### Using Planet's OrdersV2
Planet now allows you to use [ordersv2 for downloads and performing operations.

#### Third Party Tools
Using Ordersv2 to download images allows for [order management using porder tool](https://samapriya.github.io/education-research/projects/orders/#order-up-using-and-building-with-planet-s-new-ordersv2-api).
