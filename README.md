# Image-Resizing
This a asp.net mvc application to resize images by using parameter as a query string 

To implement image size option for your media content like image, just follow the following process .....

step-01:
a. get the nuget package from https://www.nuget.org/packages/ImageResizer/	
b. run in nuget console for your specific project: Install-Package ImageResizer -Version 4.2.5
 
step-02:
 a. add inside section <configuration> in web.config file for:
 <!--for image resizer-->
	<configSections>
		<section name="resizer" type="ImageResizer.ResizerSection"/>
	</configSections>
 
<system.web>
		<httpModules>	
			<!--for image resizer-->
			<add name="ImageResizingModule" type="ImageResizer.InterceptModule"/>
		</httpModules>
</system.web>

<system.webServer>		
		<modules>	
			<!--for image resizer-->
			<add name="ImageResizingModule" type="ImageResizer.InterceptModule"/>
		</modules>
	</system.webServer>
  
  <!--for image resizer-->
	<resizer>
		<plugins>
			<!-- So all the sample projects can share the same image folder-->
			<!--<add name="VirtualFolder" virtualPath="~/" physicalPath="..\Images"/>-->
		</plugins>
	</resizer>

step-03:
   a. add image tag like below format: 
   
   <div class="row">
    <div class="col-md-12 text-center">
        <h2>Getting started With Image Resizer</h2>
        <div class="row">
            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/lights.jpg">
                        <img src="~/imges/1c60deb879c1d009e2cff289199c67107c.jpg?w=200&h=200" />                        
                        <div class="caption">
                            <p>w=200&h=220</p>
                        </div>
                    </a>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/nature.jpg">
                        <img src="~/imges/Awesome-Red-Rose.jpg?w=200&h=200&mode=max&srotate=90" />                        
                        <div class="caption">
                            <p>w=200&h=200&mode=max&srotate=90</p>
                        </div>
                    </a>
                </div>
            </div>
            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/ffgsgsg.jpg?w=200&h=200&s.grayscale=true" />                        
                        <div class="caption">
                            <p>w=200&h=200&s.grayscale=true</p>
                        </div>
                    </a>
                </div>
            </div>
            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/ffgsgsg.jpg?w=200&h=200&s.sepia=true" />
                        <div class="caption">
                            <p>w=200&h=200&s.sepia=true</p>
                        </div>
                    </a>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-4">
                <div class="thumbnail">                    
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/ffsf400.png?w=200&h=220&mode=stretch" />                        
                        <div class="caption">
                            <p>w=200&h=220&mode=stretch</p>
                        </div>
                    </a>
                </div>
            </div>

            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/imddddages.jpg?w=200&h=220&mode=carve" />                        
                        <div class="caption">
                            <p>?w=200&h=220&mode=carve</p>
                        </div>
                    </a>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/imffsgsages.jpg?w=200&h=220&mode=carve" />
                        <div class="caption">
                            <p>?w=200&h=220&mode=carve</p>
                        </div>
                    </a>
                </div>
            </div>

            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/imsgsgages.jpg?w=200&h=220&mode=carve" />
                        <div class="caption">
                            <p>?w=200&h=220&mode=carve</p>
                        </div>
                    </a>
                </div>
            </div>

            <div class="col-md-4">
                <div class="thumbnail">
                    <a href="/w3images/fjords.jpg">
                        <img src="~/imges/rose-red-flower-victor-hugo.jpg?w=200&h=220&mode=carve" />
                        <div class="caption">
                            <p>?w=200&h=220&mode=carve</p>
                        </div>
                    </a>
                </div>
            </div>

        </div>


    </div>
</div>




Hopefully it will helpfull for you 
Thanks

   
   
   
   
   
   
   

