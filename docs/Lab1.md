# Lab 1 - Spatial Data Models

!!! warning "Document Version"
    Date: 29/12/2019
    
    **LibreGIS Lab Author:** Libre GIS, Germany  
    **FOSS4G Lab Author:**
    Kurt Menke, GISP
    Bird's Eye View GIS      
    **Original Lab Content Author:**
    Richard Smith, Ph.D.
    Texas A&M University - Corpus Christi
        
    The development of the original document is funded by the Department of Labor (DOL) Trade Adjustment Assistance Community College and Career Training (TAACCCT) Grant No.  TC-22525-11-60-A-48; The National Information Security, Geospatial Technologies Consortium (NISGTC) is an entity of Collin College of Texas, Bellevue College of Washington, Bunker Hill Community College of Massachusetts, Del Mar College of Texas, Moraine Valley Community College of Illinois, Rio Salado College of Arizona, and Salt Lake Community College of Utah.  This work is licensed under the Creative Commons Attribution 3.0 Unported License.  To view a copy of this license, visit http://creativecommons.org/licenses/by/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  
    This document was original modified from its original form by Kurt Menke and continues to be modified and improved by generous public contributions.
    
    **Current document (dated: 29/12/2019) is modified from its original form by LibreGIS and continues to be modified and improved by generous public contributions.**

!!! note "Objective"
    Explore and Understand Spatial Data Models

## 1. Introduction
In this lab, students will explore and manage geospatial data using *QGIS Desktop LTR version 3.4.14* and we will refer
it as QGIS for the rest of the course. QGIS is the companion application used to perform spatial analysis and to make maps. 
For data exploration, we will use **QGIS browser Panel** and for data management we will use **Data Source manager**. 

!!! note 
    Browser panel is analogous to Windows Explorer but work for geospatial data.   

This lab will also introduce the students to the QGIS interface. It is important to learn the concepts in this lab as 
future labs will require the skills covered in this lab. This lab includes the following tasks:

* Task 1 – Learn to work with QGIS browser panel.
* Task 2 – Become familiar with geospatial data models.
* Task 3 – Viewing geospatial data in QGIS desktop.

## 2. Explore and Understand Geospatial Data Models
Geographic Information Systems model the real world with representations of objects such as lakes, roads and towns. 
Geospatial data models are the means used to represent these features. They are composed to two parts:  

1. Spatial Features
2. Attributes 

Combining both will create a model of reality as illustrated in the following figure.

![Two parts of the geospatial data model](figures/Lab2/Twopartsofthegeospatialdatamodel.png "Two parts of the Geospatial data model")

There are two main geospatial data models: vector and raster. 

1. *Vector Data Model* – best for modeling discrete objects. Vector data comes in three forms: point, line and polygon.
2. *Raster Data Model* – this model is best for modeling continuous objects. A raster is composed of a matrix of contiguous cells, with each cell (pixel) holding a single numeric value.

## Task 1 - Working with QGIS Browser Panel
In this task, you will become familiar with QGIS Browser Panel. The first step in working on a project with 
geospatial datasets is to organize your workspace. It is important that we organize datasets logically on 
the computer and make them easy to find. In this task, you will obtain a copy of the lab1 data under `GST101_Data\Lab1_data\` and explore how the data is organized using QGIS Browser Panel. 



1.	Click Start | QGIS 3.4 | QGIS Desktop 3.4.14 as shown in the following figure.  
    
    ![QGIS Start](figures/Lab2/qgis_start_menu.png "QGIS Desktop with browser panel")
    
    This will open QGIS 3.4 Desktop as shown in the following figure. This interface is simple and clean.
    Browser panel is visible on top left side and shows all the aviable files and folder 
    
    !!! note 
        Your machine may have a different set and number of drives listed here and this is fine.
    
    Below the drives are Database Connections and there are no connections to any databases at this point. 
    On top bottom side you will see layer menue, on right side Map Canvas and on the top you will see Main menu bar and several toolbars, which will be explained thoughout the rest of the labs.
    
    ![QGIS Browser](figures/Lab2/QGIS_Browser.png "QGIS Browser")

2.	Look at the file tree in the Browser Panel. Click the arrow to the left of the ``C:`` drive. You will now see all of the subfolders directly under the ``C:\`` folder.

3.	Expand the `GST101_Data\Lab1_data` folder where you stored your data in the File Tree by clicking the arrows to the left of each folder. You will now see the contents of the Data folder for the lab (shown in figure below).

    ![Lab Data in QGIS Browser](figures/Lab2/Lab_Data_in_QGIS_Browser.png "Lab Data in QGIS Browser")

4.	Take a moment to read the names of the files. There are two folders and several files listed with different icons. The ![Vector Icon ](figures/Lab2/Vector_Icon.png "Vector Icon") icon indicates that the dataset is a vector layer. This icon ![Raster Icon ](figures/Lab2/Raster_Icon.png "Raster Icon") is used to represent raster data but is also used for other files such as the XML files you see here.

5. Look at the Browser panel. Note that there is a Favourites item. Identify folders or locations as being Favourites in order for them to appear here. 
   Data is often stored deep inside a series of folders. It is often tedious and time consuming to navigate deep inside the folders to gain access to the data. 
   Favourites provide a way to create a shortcut directly to any folder so that you have one-click access to any folder. 
   Let's create a favorite to our lab folder for practice.

6. Navigate to the ``GST101\Lab1_data`` folder in the browser panel. Right-click on it and choose Add as a Favourite (see figure below).
   Once set, ``GST101\Lab1_data`` folder will show up under Favourite.  

    ![Add as a Favourite](figures/Lab2/qgis_add_faviourities.png "Add as a Favourite")
      

7. Now expand Favourites and you will see your ``GST101\Lab1_data`` folder listed there. You can remove a favourite anytime by right-clicking on it and choosing Remove favourite.
8. Expand the ``GST101\Lab1_data`` folder under Favourites to expose the contents. Select SDOT_StateRoutes.shp and drag it onto the map. This is a quick way to add data to your map. 


## Task 2 - Become familiar with geospatial data models

Now that you are familiar with the basic layout of QGIS Browser panel, we will explore some geospatial data.

1.	Let’s take a closer look at the data in ``GST101\Lab1_data`` folder in QGIS Browser panel.
2.	Select the Hawaii_Counties.shp layer in the file tree. Now right click and select *properties* from context menu.
    This will open up layer properties window and Metadata tab will be shown by default. 
    This gives you some basic information about the dataset. 
    You’ll notice that the Storage type is ESRI shapefile. The Display Window also tells you that it has a Geometry type of polygon and it has 9 features (shown in figure below).
    
    ![Metadata in QGIS Browser](figures/Lab2/Metadata_in_QGIS_Browser.png "Metadata in QGIS Browser")

    In addition to data models (vector and raster) we have to understand file formats. Some file formats are designed to store vector and others raster data. Shapefiles are vector file format. In fact they are probably the most common vector file format. An individual shapefile can only contain one geometry type (polygon, line, or point). A shapefile is actually a collection of files on the computer with a common name, but different extensions.

3.	Now select PubSchools.shp and check it's properties. You’ll see that this is also an ESRI Shapefile but that it is a point dataset with 287 features.
4.	Select SDOT_StateRoutes.shp and check it properties. This is an ESRI Shapefile with line geometry and 122 features. 
5.	Select Hawaii_Counties.shp again and click on the properties and then select Preview tab from Layer Properties. 
    This shows you the spatial features of this GIS dataset (shown in figure below )

    ![Preview in QGIS Layer Properties](figures/Lab2/qgis_layer_preview.png "Preview in QGIS Layer Properties")

6.	Click on the Attributes tab in the Layer Properties dialog. This shows you the other component of the data model, the attributes. Each row corresponds to one polygon. The columns are things we know about the polygons such as island name (see figure below).

    ![Attributes in QGIS Layer Properties Dialogue](figures/Lab2/qgis_layer_attributes.png "Attributes in QGIS Layer Properties Dialogue")

7.	Select the Oahu_Landsat_15m.jp2 dataset. Open properties and then click on the Preview tab. This is an example of a raster dataset. Like a photograph, it is composed of cells. This raster is a satellite image of the island of Oahu, Hawaii (shown in figure below).

    ![Raster data Preview](figures/Lab2/qgis_raster_preview.png "Raster data Preview")
    

## Task 3 - Viewing geospatial data in QGIS Desktop

Now that you know how geospatial datasets are stored on your computer, let’s see what the data they contain look like. 

1. QGIS Desktop is the application you will use for making maps, editing data, and doing GIS analysis, among many other operations. 
    As we have already seen in [Task1](#task-1---working-with-qgis-browser-panel) that QGIS Desktop has several sections e.g. the Layers panel, the browser panel and the Map Canvas.

    !!! note 
        Your QGIS Desktop window may look slightly different than the one pictured above. To reset your display back to the default settings, 
        click Settings | Options | System tab | Settings section | Reset button, then click OK and restart QGIS Desktop.
        
    The QGIS Desktop interface is a little cluttered by default, so let's close a few panels so we just see the Layers panel and Map Window.

2. Locate the *Browser* panel, and click the small 'X' button in the upper-right corner to close the panel.

3. Panels can be docked and undocked from the QGIS Desktop window. To undock a panel, click and drag the panel's top title bar (outlined in figure below) and drag it away from the sides. When you release your mouse button, the panel will be floating freely.
    
    ![Area to Drag When Undocking a Panel](figures/Lab2/qgis_layer_drag.png "Area to Drag When Undocking a Panel")

    To dock a floating panel, click and drag the title bar, and drag the panel to the left or right side of QGIS Desktop until a rectangle appears underneath the panel. Release the mouse button to dock the panel (docking action shown in figure below).

    ![Docking the Layers Panel](figures/Lab2/qgis_layer_brwoser_stacked.png "Docking the Layers Panel")

    With the QGIS Desktop interface customized, let’s add some data. 

4. Click the data source manager icon ![data source manager icon](figures/Lab2/qgis_data_source_manager.png "data source manager icon") in QGIS toolbar. It will open Data Source Manager.  
    
    ![data source manager browser](figures/Lab2/qgis_data_source_browser.png "data source manager browser")

### Task 3.1 - Add Vector Data
    
1. Now click on Vector icon in the left panel. This opens the Add vector layer panel on the right side. Alternatively goto menu and click `Layer → Add Layer → Add Vector Layer`.
    ![Add Vector Layer](figures/Lab2/qgis_data_source_vector.png "Add Vector Layer") 
    
2. Let's add one of the ESRI shapefiles which is a file-based dataset. Click the Browse button. 

3. The *Open an OGR Supported Vector Layer* window opens.  The window defaults to all files. From exploring the lab data in QGIS Browser, 
    you know there are several shapefiles in the lab data folder. Take a moment to see the other available options.
    Click the All files dropdown box and change to ESRI Shapefiles (shown in figure below).
    
    !!! note 
        OGR is a FOSS4G project with the sole purpose to read and write geospatial vector data files.
        
    ![OGR Supported Vector Formats](figures/Lab2/qgis_org_provider_list.png "OGR Supported Vector Formats")

            
4. Once you are finished exploring, make sure it is still set to ESRI Shapefiles. This filters what you can see in the lab folder so that you only see the shapefiles. 
5. Select Hawaii_Counties.shp and click OK.
6. Now back on the Data Source Manager window and click Add to add the data to QGIS Desktop.
7. You will now see Hawaii_Counties in the Layers panel and the map features displayed in the map window. 
    Vector GIS layers will come in with a random colors. You will learn how to change layer styling in a future lab. 
8. Let’s examine the attributes. Right-click on the Hawaii Counties layer in the Layers panel. This opens a context menu. Select Open Attribute Table (shown in figure below).

    ![Layer Context Menu](figures/Lab2/qgis_properties_attribute_table.png "Layer Context Menu")

9. The attribute table opens. If you recall from exploring this dataset with QGIS Browser, it has 9 features (9 polygons). The attribute table has 9 corresponding records. There are columns with the County name (NAMELSAD10) and with the Island name (Island). Close the Attribute Table by clicking the X button in the upper right hand corner.

    ![Attribute Table](figures/Lab2/qgis_hawei_attribute_table.png "Attribute Table")

10. Another way to interact with both the spatial features and the attributes is the Identify button.
11. Click the Identify button ![Identify Button](figures/Lab2/Identify_Button.png "Identify Button")
12. Click on one of the features on the map. The Identify results panel (shown in figure below) shows you the attributes for the feature you clicked on. *Note:* The Identify results panel may initially be docked or floating.
    
    ![Identify Results](figures/Lab2/qgis_identify_attributes.png "Identify Results")
    
### Task 3.2 - Add Raster Data
Now you will learn how to add Raster data to QGIS Desktop.

1. Click the Raster Layer button ![Add Raster Layer button](figures/Lab2/Add_Raster_Layer_button.png "Add Raster Layer button") in Data Source Manager window.  
   Alternatively go to menu and click `Layer → Add Layer → Add Raster Layer`.
2. The Open a GDAL Supported Raster Data Source window opens (displayed in figure below). This is a very similar workflow to adding vector data.
    
    ![Open a GDAL Supported Raster Data Source](figures/Lab2/qgis_add_raster.png "Open a GDAL Supported Raster Data Source")

3. Whereas QGIS used OGR to open vector data files, here it uses another FOSS4G software library called GDAL. GDAL is used for reading and writing raster datasets. 
4. The window’s raster data filter is set to All Files by default, so you see the entire contents of the folder.
5. Set the filter to JPEG2000. (Also, note how many formats it will read!) In GIS there are many more raster file types than vector. Once you’ve set the filter you’ll see the one dataset: Oahu_Landsat_15m.jp2.
6. Select the Oahu_Landsat_15m.jp2 raster dataset and click Open. Now you will be returned back to the Data Source Manager Window. Click on Add and this data will be added to the layer panel.

7. This dataset only covers a portion of Hawaii, just the island of Oahu. Right-click on the Oahu_Landsat_15m dataset in the layers panel and choose Zoom to Layer to zoom to the spatial extent of this raster (shown in figure below).

    ![Zoom to Layer](figures/Lab2/qgis_raster_zoom.png "Zoom to Layer")

    You may notice two folders in the lab data folder that we have not discussed yet. One is named *hilloah* and the other *info*. Together, these combine to make another geospatial raster dataset format named GRID.  The info folder holds the attributes and always has the name "info". The other folder is the layer name and contains the spatial data. Let's add a GRID raster to our map.

8. Now click again on the Raster Layer button ![Add Raster Layer button](figures/Lab2/Add_Raster_Layer_button.png "Add Raster Layer button") in Data Source Manager window.
   
9. Click on browse button and a new file dialogue will open. Set the filter to Arc/Info Binary Grid. Double click the hilloah folder to enter it. Select the hdr.adf file and click Open to add the raster to QGIS (shown in figure below).
   ![Adding a GRID to QGIS](figures/Lab2/qgis_add_arc_info.png "Adding a GRID to QGIS")
    
10. This raster is a hillshade image of Oahu and it represents the terrain.

!!! note
    You can drag data from the QGIS Browser application to QGIS Desktop as well to add the data to the map. 

## 5. Conclusion
In this lab you explored datasets that use the two common geospatial data models: vector and raster. You have also used the QGIS Browser to preview datasets. In future labs, you will learn how to use QGIS Desktop to make maps and perform analysis. 

## 6. Discussion Questions
1. What are the 14 possible file extensions for files that compose a shapefile?
2. How can Browser favourites make your workflow more efficient?
3. What are the two main parts of a GIS data model?
4. Name three ways of seeing feature attributes for a vector GIS layer.