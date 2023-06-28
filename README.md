# Data Profiling

* This code takes the top 10,000 rows of each table & view inside of GVR_DEV ERP databases
* These databases include:
    * AS400_GER
    * AX
    * HFM
    * MAC-PAC 
    * PROTHEUS_AR
    * PROTHEUS_BR
    * PROTHEUS_CH
    * QAD
    * SMS

# Recommendations for Running Code (Important - Please Read!)
* This code collects data from hundreds of tables and views in large databases. The code will take a very **long** time to load **(hours)** if you're running through all ERP schemas. It is my recommendation to run this code in the background during your day and occassionaly check on if the code cell currently running is complete or not.
* All ERP tables have been uploaded already, the code needed to run specific tables in specific schemas is located at the bottom on the .IPYNB file

# Instructions

## Install Anaconda & Visual Studio Code

* This process requires the installation of Anaconda & Visual Studio Code
* Please ensure installation of these applications:
    * Visual Studio Code installation found <a href="https://code.visualstudio.com/download" target="_blank">here</a>
    * Anaconda installation found <a href="https://docs.anaconda.com/free/anaconda/install/index.html" target="_blank">here</a>

------

## Clone Repository

* Copy HTTPS

<p>
  <img 
    src=Photos/git_clone.png
  >
</p>

* Navigate to Anaconda Command Prompt and run the command below:

<p>
  <img 
    src=Photos/git_clone_command.png
  >
</p>

------

## Create Virtual Environment

* Navigate to your Anaconda Command Prompt
* Create a virtual environment with a specific python version (3.8.15)
    * To change name of virtual environment switch out 'test' for another name

<p>
  <img 
    src=Photos/create_env.png
  >
</p>

* Activate virtual environment

<p>
  <img 
    src=Photos/activate_env.png
  >
</p>

* Run module downloads (pip install, conda install, OR conda install -c conda-forge (**this one is good at collecting metadata when the other commands won't**))
    * Snowflake-snowpark-python
    * Dataprep
    * Pandas
    * Shutil
    * Office365-rest-client

<p>
  <img 
    src=Photos/install_module_example.png
  >
</p>

------

## Run Code

* While still inside of the Anaconda Command Prompt, navigate to the location this repository was cloned using the 'cd' command
    * Run 'code .'
* Navigate to the .IPYNB file inside of the repository in Visual Studio Code
* Select correct kernel to use
    * This will be the virtual environment created earlier in this process

<p>
  <img 
    src=Photos/select_kernel.png
  >
</p>

<p>
  <img 
    src=Photos/kernel_pop.png
  >
</p>

* Go to the Python Environments selection and select environment

* All modules should appear similarly to this:
    * If this does not appear similarly to the photo above either try: restarting the kernel or closing out of Visual Studio Code & reopening the application through your Anaconda Command Prompt

<p>
  <img 
    src=Photos/dependencies.png
  >
</p>

* Change out all occurences of 'emily.porter@gilbarco.com' and replace with work email address and replace the role with appropriate an role name

* Once you run the .IPYNB file you will see HTML files populating your sidebar

<p>
  <img 
    src=Photos/html_populating.png
  >
</p>

* After each cell is done running, a new authentication window will automatically load into your browser


* These HTML files will be placed into a separate folder inside GVR_DEV. Once all code has been completed:
  * Locate SharePoint file <a href="https://vontier.sharepoint.com/sites/GVR-DataAnalytics/Shared%20Documents/Forms/AllItems.aspx?csf=1&web=1&e=imhEE4&OR=Teams%2DHL&CT=1685019593535&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMzA0MDIwMjcwNSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D&cid=6d63efe9%2Dde99%2D4f3f%2Dbb5b%2D00cf7172156a&FolderCTID=0x012000C6F5B059D3922D44BEAB03F40E9D9AB8&id=%2Fsites%2FGVR%2DDataAnalytics%2FShared%20Documents%2FGeneral%2F1%2E%20DA%20Document%20Management%20System%2F5%2E%20Artifacts%2FData%20Lake%20Artifacts%2FData%20Profiling&viewid=1735308e%2Da40f%2D4ff1%2D8987%2D77fd3877b77c" target="_blank">here</a>
  * Upload files created to appropriate schema


# Running Only One Table?
* Refer to the last cell of code inside of the .IPYNB file
* Replace schemas & table/view names inside this cell

# View Reports
* The .HTML files are uploaded to SharePoint by the user where they will be viewable. For full interactivity download the .HTML file and view the table desired
* These results will look like this:
* A high-level overview is included that includes information on number of rows, missing cells & missing cell %, duplicate rows & duplicate row %, cardinality, and skewed data

<p>
  <img 
    src=Photos/html_output.png
  >
</p>

* This report also provides users with insights into column-level data

<p>
  <img 
    src=Photos/html_output2.png
  >
</p>


# Questions

* You can contact me via email or GitHub!
    * Email: emilyporter920@gmail.com
    * GitHub Profile: Emily Porter || https://www.github.com/emilyporter920 
