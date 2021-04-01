# Reference Sample - cadviewer-testapp-vue-01

This CADViewer Example is a reference implementation of CADViewer on Vue JS.

## Install CADViewer VueJS Sample

```
npm i cadviewer-testapp-vue-01
```

**NOTE: Please use [Github](https://github.com/CADViewer/cadviewer-testapp-vue-01) to download/clone this sample: [cadviewer-testapp-vue-01](https://github.com/CADViewer/cadviewer-testapp-vue-01) as the preferred route!** 



Once the sample is up running, you need to install and connect to our NodeJS conversion server for handling of CAD files. 




## Install CAD Conversion Server


Download the CADViewer Node JS CAD Conversion server (or alternatively the PHP, .NET or Servlet Server implementations).

Go to: [https://cadviewer.com/download/](https://cadviewer.com/download/), register and receive email and then download from the section **CADViewer Handler/Connector Scripts**. Follow the instructions on the download page.






## Install Converters

Download the CAD Converter [AutoXchange 2020](https://tailormade.com/ax2020techdocs). 

Go to: [https://cadviewer.com/download/](https://cadviewer.com/download/), register and receive email and then download from **AutoXchange 2020 Downloads**.

Place the Converter as part of the CAD Conversion server structure, typically: */converters/ax2020/windows* or */converters/ax2020/linux*. See instructions on download page on how to set up paths and fonts folders.





## Reference Samples  - Alternative user controlled installation

### Setup of sample and npm installation of CADViewer

Install Vue CLI on your computer and run the command

```
vue create cadviewer-testapp-vue-01
```


In folder cadviewer-testapp-vue-01, install CADViewer. 

```
npm i cadviewer
```

For the sample methods, remove hard method syntax checking:

```
npm uninstall @vue/cli-plugin-eslint
```




### Modify App.vue


In the main **src/App.vue**, we add three new components. The main CADViewer canvas component, and then two components CADViewerHelperMethods that illustrates working with the CADViewer API to highlight and control objects on the canvas and CADViewerSpaceObjects which illustrates how to select and add SVG or bitmap objects to the CADViewer canvas as interactive Space Objects.



{{< gist CADViewer 3266556eafb3e8728894781422568606 "vuejs_docs_132.vue" >}}


### Modify main.js 


In **src/main.js** , add the declaration of an eventbus which allows the tree CADViewer components to exchange method calls between them. 

```
export const eventBus = new Vue(); // added to trigger inter components call of methods
```


### Add CADViewer components 


Download the [CADViewer Vue components](https://cadviewer.com/downloads/handlers/vuejs/vuejs_sample.zip) and add them to the **/src/components/** folder structure.


Sample component vue files:

 * CADViewerCanvas.vue
 * CADViewerHelperMethods.vue
 * CADViewerSpaceObjects.vue
 
(the download zip also includes a modified HelloWorld.vue file)

### Add CADViewer content to /public/ 


There are some general image and XML configuration files that CADViewer needs during execution, please download [vue_react_public_folder_cadviewer_6_4.zip](https://cadviewer.com/downloads/handlers/reactjs/react_public_folder_cadviewer_6_4.zip) and place in your VueJS /public/ project folder.   



**NOTE:** Follow instructions to install NodeJS conversion server and Converters.

**NOTE2:** You can install this sample from Github; **[cadviewer-testapp-vue-01](https://github.com/CADViewer/)**.







## Bookkeeping paths


Note that the path book-keeping in your main *.vue file invoking CADViewer is important for proper initialization, where the ServerBackEndUrl and ServerLocation is the location and Url of the CAD Server and ServerUrl is the Url of the VueJS application encapulating CADViewer. 


		var ServerBackEndUrl = "http://127.0.0.1:3000/";
		var ServerUrl = "http://localhost:8080/";
		var ServerLocation = "c:/nodejs/cadviewerServer/";





## General Information


**LICENSE: TMS 1.0:** Use freely on localhost. Commercial use requires licensing, both using entirely or in parts. Forbidden to remove license key check.  Contact Tailor Made Software, https://cadviewer.com/contact , for more information. 

Use the [CADViewer API](https://cadviewer.com/cadviewerproapi/global.html) to open and manipulate drawings in your application. 

Use our five guides to learn to manipulate interactive content:

Read the Guide on how to **[create hotspots](https://cadviewer.com/highlight/main/)** (Space Objects), it outlines how spaces can be processed on a drawing to create interactive objects. 

Read the Guide on how to **[add or modify hotspots & imgages ](https://cadviewer.com/highlight2/main/)**  (Space Objects), this will help you work with the code in this sample. 

Read the Guide on how to **[style hotspots](https://cadviewer.com/highlight3/main/)**  (Space Objects).

Read the Guide to introduce **[The Canvas API](https://cadviewer.com/highlight4/main/)**.

And finish off by learning how to  **[Retain AutoCAD Handles](https://cadviewer.com/handles/main/)** in drawings.


Read the general documentation on **CADViewer** is found at: https://cadviewer.com/cadviewertechdocs/ .

The general documentation on **AutoXchange 2020** is found at: https://tailormade.com/ax2020techdocs/ .

The CADViewer API is found at: https://cadviewer.com/cadviewerproapi/global.html .



## CADViewer Sample

The sample loads a drawing with interactive Spaces, Area Calculation on Spaces, as well as helper methods to do various interaction with CADViewer.



![CADViewer VueJS](https://cadviewer.com/images/cadviewer/reactjs_canvas.png "CADViewerApp VueJS")


